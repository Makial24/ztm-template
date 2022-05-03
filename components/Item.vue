<template>
    <dir class="border rounded-md border-grey-200 text-left pb-5">
        <img :src="image" alt="">
        <h3 class="font-oswald font-medium text-2xl uppercase mt-5 mb-2 ml-5">
            {{ title}}
            </h3>
        <p class="font-light text-blue-800 mb-2 ml-5">
            {{ description}}
            </p>
        <span class="bg-amber-800 text-yellow-400 font-bold text-xl font-oswald rounded rounded-lg px-4 py4 ml-5">
            RM {{ price}}
            </span>
    </dir>
</template>

<script>
export default {
  props: ['image', 'title', 'description', 'price']
}
</script>
