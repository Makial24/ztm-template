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
        <h1 class="text-white font-oswald uppercase text-6xl text-center pt-16 pb-24">Shopping Cart</h1>
        </div>
        <table class="table-auto w-2/3 mt-20 mx-auto">
            <thead>
                <tr>
                    <th class="text-left">Name</th>
                    <th class="text-center">Price</th>
                    <th>Quantity</th>
                    <th class="text-center">Total</th>
                    <th>Remove</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="order in $store.state.orders" :key="order.name" class="font-oswald uppercase text-2xl border-b">
                    <td class="py-10">{{ order.name }}</td>
                    <td class="text-right">RM {{ order.price.toFixed(2) }}</td>
                    <td class="text-center">{{ order.quantity }}</td>
                    <td class="text-right">RM {{ (order.price * order.quantity).toFixed(2) }}</td>
                    <td class="text-center"><button @click="removeItem (order,name)">❌</button></td>
                </tr>
            </tbody>
            <tfoot>
                <tr class="font-oswald text-2xl bg-gray-100 uppercase font-bold">
                  <td class="py-10" colspan="3">Total</td>
                  <td class="text-right">RM {{ total.toFixed(2) }}</td>
                </tr>
                <tr>
                  <td colspan="3">
                    <input id="email" type="email" placeholder="Please enter your email" class="w-full border border-gray-300 text-xl mt-5 px-2 py-3">
                  </td>
                  <td colspan="2" class="text-right">
                    <button class="font-oswald uppercase bg-red-500 text-white text-xl py-3 px-2 ml-5 mt-5" @click="submitOrder">Confirm my order</button>
                  </td>
                </tr>
            </tfoot>
        </table>
    </div>
    </template>

<script>
export default {
  computed: {
    total() {
      let total = 0;
      this.$store.state.orders.forEach((orders) => {
        total = total + (orders.price * orders.quantity);
      })

      return total;
    },
  },

  methods: {
    removeItem(name) {
      this.$store.commit('removeItem', name);
    },
    submitOrder() {
      this.$axios.post('/.netlify/functions/email', {
        email: document.getElementById('email').value,
        orders: this.$store.state.orders,
      })
        .then(function (response) {
          alert('Your order has been submitted');
        });

      this.$axios.post('/.netlift/functions/db', {
        email: document.getElementById('email').value,
        orders: this.$store.state.orders,
      })
    }
  }
}
</script>
