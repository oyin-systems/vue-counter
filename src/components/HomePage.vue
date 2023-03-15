<template>
    <div class="font-sans">
        <h1 class="m-30">Counter App</h1>
        <p class="mt-20 mb-20 text-2xl font-bold leading-loose">Hey there! This is a Simple Counter Application built with Vue JS<br/>and it has the Increment, Decrement, SetValue and Reset functions.</p>

    <div>
        <button type="button"> <router-link to="/counter" class="border-2 border-teal-500 px-4 py-2 hover:bg-teal-500 hover:text-white mr-10 text-xl font-bold">Counter</router-link> </button>
        <button type="button"> <router-link to="*" class="border-2 border-teal-500 px-4 py-2 hover:bg-teal-500 hover:text-white text-xl font-bold">404 Page</router-link> </button>
    </div>
</div>
</template>

<script>
export default {
    name: 'HomePage'
}
</script>