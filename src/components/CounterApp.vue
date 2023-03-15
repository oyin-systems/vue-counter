<template>
  <div>
    <h2 class="text-3xl font-bold text-gray-800 mt-20 pt-10 mb-10">
      Counter: {{ count }}
    </h2>
    <div>
      <button
        @click="decrement"
        class="border-2 border-teal-500 px-4 py-2 hover:bg-teal-500 hover:text-white mr-5 mb-10 text-2xl rounded-xl"
      >
        Decrement
      </button>
      <button
        @click="increment"
        class="border-2 border-teal-500 px-4 py-2 hover:bg-teal-500 hover:text-white text-2xl rounded-xl"
      >
        Increment
      </button>
    </div>
    <div class="p-5 w-auto flex justify-center items-center">
      <input type="number" v-model="value" class="py-2 px-4 text-2xl border-2 border-teal-500" />
      <input
        type="submit"
        @click="setValue(value)"
        value="Set Value"
        class="text-2xl text-white border-2 border-teal-500 px-4 py-2 hover:bg-white hover:text-teal-500 text-2xl bg-teal-500 font-bold"
      />
    </div>
    <button
      @click="reset"
      class="border-2 border-teal-500 px-4 py-2 hover:bg-teal-500 hover:text-white mt-10 text-2xl rounded-xl"
    >
      Reset
    </button>
  </div>
</template>

<script>
import useCounter from "@/composables/counter";

export default {
  setup() {
    const { count, increment, decrement, reset, setValue } = useCounter();

    return {
      count,
      increment,
      decrement,
      reset,
      setValue,
      value: 0,
    };
  },
};
</script>

<!-- <style scoped>
    .counter{
      display: flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      max-width: 100vw;
      margin: 0 auto;
      height: calc(100vh - 60px);
      flex-direction: column;
      animation: fadeIn 1s ease-in-out;
    }
    .heading-main{
      font-size: 48px;
      margin-bottom: 16px;
      text-align: center;
      font-family: primaryFont;
      font-weight: bolder;
    }
    .btn-wrapper{
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 10px;
      margin: 10px;
    }
    .btn{
      width: 100px;
      height: 50px;
      font-weight: 600;
      font-size: 18px;
      font-family: primaryFont;
      outline: none;
      border: none;
      border-radius: 10px;
      color: black;
    }
    .btn.reset{
      background-color: azure;
    }
    .btn.reset:hover{
      background-color: #4682B4;
      color: white;
      transition: all 0.4s;
    }

    .btn.increment{
      background-color: #4682B4;
    }
    .btn.increment:hover{
      background-color: #6495ED;
      color: white;
      font-weight: bolder;
      transition: all 0.4s;
    }

    .btn.decrement{
      background-color: #89CFF0;
    }
    .btn.decrement:hover{
      background-color: #6495ED;
      color: white;
      font-weight: bolder;
      transition: all 0.4s;
    }
    .input-wrapper{
      width: 98%;
      margin: 0 auto;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    input{
      border: none;
      height: 50px;
      padding: 10px;
      width: 260px;
      margin: 20px 0 20px 0;
      font-family: primaryFont;
      font-size: 16px;
    }
    .input-field{
      border-radius: 10px 0 0 10px;
      outline: none;
    }
    .submit{
      border-radius: 0 10px 10px 0;
      margin-left:  -4px;
      border-left: 1px solid #fff;
      font-weight: bolder;
      width: 100px;
      padding: 10px;
    }
    .submit:hover{
      background-color: azure;
      transition: all 0.4s;
    }

    @keyframes fadeIn {
      0% {
        opacity: 0;
      }
      100% {
        opacity: 1;
      }
    }
</style> -->
