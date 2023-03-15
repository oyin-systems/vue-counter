<template>
  <nav class="flex items-center justify-between flex-wrap bg-[#14b8a6] p-6 top-0 w-full fixed">
    <div class="text-white text-3xl font-bold font-mono">CounterApp</div>
    <div>
      <ul>
        <li class="sm:inline-block font-extrabold"><router-link to="/" class="mr-10 p-3 hover:text-white outline-white outline outline-2  outline-offset-2 ...">Home</router-link></li>
        <li class="sm:inline-block font-extrabold"><router-link to="/counter" class="p-3 hover:text-white outline-white outline outline-2  outline-offset-2 ...">Counter</router-link></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavBar",
};
</script>
