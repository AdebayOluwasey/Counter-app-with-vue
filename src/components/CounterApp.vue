<template>
  <div class="counter">
    <h1 class="heading">Counter:{{ count }}</h1>
    <div class="input-wrapper">
      <input class="input-field" type="number" v-model="value" />
      <button class="btn setvalue" @click="setValue(value)">SetValue</button>
    </div>
    <div class="btn-wrapper">
      <button class="btn increment" @click="increment">+</button>

      <button class="btn decrement" @click="decrement">-</button>
    </div>
    <button class="btn reset" @click="reset">Reset</button>
  </div>
</template>

<script>
import useCounter from "../composables/counter";

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

<style scoped>
.counter {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 60px;
  height: calc(100vh-60px);
  width: 100%;
  max-width: 100vw;
  margin: 0 auto;
  animation: fadeIn 1s ease-in-out;
}

.heading {
  font-size: 3rem;
  text-align: center;
  font-weight: bolder;
  margin-bottom: 16px;
  font-family: primaryFont;
}

.input-field {
  border-radius: 10px;
  outline: none;
}
input {
  height: 50px;
  width: 250px;
  padding: 10px;
  font-family: primaryFont;
  font-size: 16px;
  margin: 20px 0 20px 0;
}
.input-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  margin: 10px;
}
.btn-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  margin: 10px;
}
.btn {
  width: 100px;
  font-size: 18px;
  height: 50px;
  font-weight: 600;
  border-radius: 10px;
  border: none;
  outline: none;
  font-family: "Times New Roman", Times, serif;
  box-shadow: 3px 3px 6px 555;
}
.btn.increment {
  background-color: #6495ed;
  color: black;
}
.btn.increment:hover {
  background-color: white;
  font-weight: bolder;
  transition: all 0.4s;
}

.btn.decrement {
  background-color: skyblue;
  color: black;
}
.btn.decrement:hover {
  background-color: azure;
  font-weight: bolder;
  transition: all 0.4s;
}

.btn.reset {
  background-color: darkcyan;
  
}
.btn.reset:hover {
  background-color: azure;
  border-radius: 10px;
  transition: all 0.4s;
}

.btn.setvalue {
  background-color: aliceblue;
  color: black;
}
.btn.setvalue:hover {
  background-color:cornflowerblue;
}

input {
  font-size: 16px;
  font-family: "Courier New", Courier, monospace;
  border: none;
  margin: 20px 0 20px 0;
  width: 260px;
  height: 50px;
  text-align: center;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
