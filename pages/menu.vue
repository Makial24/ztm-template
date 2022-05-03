<template>
    <div>
        <div class="bg-[url('/menu-page.jpg')] px-20">
            <div id='menu' class="grid grid-cols-2 py-5">
                <div id='menu-left'>
                    <img src="logo.png" class="w-[100px]" alt="">
                </div>
                <div id='menu-right'>
                    <ul class="grid grid-cols-5 test-lg font-oswald text-white pt-10">
                        <li>About Us</li>
                        <nuxt-link to="/menu">Our Menu</nuxt-link>
                        <li>Locations</li>
                        <li>Contacts</li>
                        <nuxt-link to="/cart">Cart
                        ({{ $store.getters.totalItems}})
                        </nuxt-link>
                    </ul>
                    </div>
                </div>
            <h1 class="text-white font-oswald uppercase text-6xl text-center pt-24 pb-28">Our Menu</h1>
        </div>
        <div id='items' class="grid grid-cols-3">
            <MenuItem v-for="b in items"
            :key='b.name'
            :item='b' />
        </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      items: []
    }
  },
  mounted() {
    this.$axios.get('items.json').then(
      (respond) => {
        this.items = respond.data.burgers;
      })
  }
}
</script>
