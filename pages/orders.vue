<template>
    <div>
        <div class="bg-[url('/menu-page.jpg')] px-20">
        <div id="menu" class="grid grid-cols-2 py-5">
            <div id="menu-left">
                <img src="logo.png" class="w-[150px]" alt="">
            </div>
                <div id="menu-right">
                    <ul class="grid grid-cols-5 test-lg font-oswald text-white pt-10">
                        <li>About Us</li>
                        <nuxt-link to="/menu">Our Menu</nuxt-link>
                        <li>Locations</li>
                        <li>Contacts</li>
                    <nuxt-link to="/cart">Cart</nuxt-link>
                    </ul>
                </div>
            </div>
            <h1 class="text-white font-oswald uppercase text-6xl text-center pt-16 pb-24">orders</h1>
        </div>

        <div v-if="user === null" id="login" class="text-center mt-20">
            <p>This page is limited to authorized users only</p>
            <button class="font-oswald uppercase bg-red-500 text-white py-3 px-3 rounded rounded-lg" @click="login">Login</button>
        </div>

        <div v-if="user" id="logout" class="text-center mt-20">
            <button class="font-oswald uppercase bg-red-500 text-white py-3 px-3 rounded rounded-lg" @click="logout">Login</button>
        </div>

        <table v-for="order in orders" :key="order.id" class="table-auto w-2/3 mt-20 mx-auto">
            <thead>
                <tr>
                    <td colspan="4">
                        <h1 class="font-oswald uppercase test-2xl pb-10">
                            order ID - {{ order.id }}
                        </h1>
                    </td>
                </tr>
                <tr>
                    <th class="text-left">Name</th>
                    <th class="text-center">Price</th>
                    <th>Quantity</th>
                    <th class="text-center">Total</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in order.data.orders" :key="item.name" class="font-oswald uppercase text-2xl border-b">
                    <td class="py-10">{{ item.name }}</td>
                    <td class="text-right">RM {{ item.price.toFixed(2) }}</td>
                    <td class="text-center">{{ item.quantity }}</td>
                    <td class="text-right">RM {{ (item.price * item.quantity).toFixed(2) }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
  data() {
    return {
      orders: [],
      user: {}
    };
  },

  head() {
    return {
      script: [
        {
          src: 'https://identity.netlify.com/v1/netlify-identity-widget.js'
        }
      ]
    }
  },

  mounted() {
    this.user = window.netliftIdentity.currentUser()
    if (this.user) {
      this.readOrders();
    }
  },

  methods: {
    readOrders() {
      this.$axios.get('/.netlify/functions/readorders', {
        Headers: {
          Authorization: `Bearer ${this.user.token.access_taken}`,
        },
      })
        .then((response) => {
          this.orders = response.data;
        });
    },

    login() {
      window.netliftIdentity.open();
      window.netliftIdentity.on('login', (user) => {
        this.user = user;
        this.readOrders();
      });
    },

    logout() {
      window.netliftIdentity.logout();
      this.user = null;
      this.orders = [];
    }
  },
};
</script>
