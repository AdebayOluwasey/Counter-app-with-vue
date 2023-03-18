<template>
  <main class="main-app">
    <h1 class="main-heading">Counter App</h1>
    <p class="Homepage-msg">
      Welcome to my counter app built with VueJs.It can perform functions like
      Increment, decrement, reset and SetValue
    </p>

    <div class="btn-wrap">
      <button type="button" class="btn">
        <router-link to="/counter">Counter</router-link>
      </button>
    </div>
  </main>
</template>

<script>
export default {
  name: "HomePage",
};
</script>

<style>
/*...*/
.main-app{
display: flex;
flex-direction: column;
justify-content: center;
padding: 30px;
align-items: center;
gap: 20px;
border: none;
height:calc (100vh-80px);
width:98%;
margin: 0 auto;
animation: fadeIn 1.5s ease-in-out;

}
.main-heading {
  font-size: 54px;
  margin-bottom: 16px;
  text-align: center;
  font-weight: bolder;
  font-family: primaryFont
}

.Homepage-msg {
  font-size: 18px;
  font-family: terFont;
  text-align: center;
  display: flex;
  flex-direction: column;
  gap: 20px;
  margin:0 auto;
  width:100%;
  justify-content: center;
  align-items: center;
}

.btn-wrap .btn {
  width: 100px;
  height: 50px;
  outline: none;
  border: none;
  border-radius: 10px;
  font-family: terFont;
  font-size: 20px;
  background-color: aliceblue;
  margin: 10px;
  filter: drop-shadow(0 0 1em aliceblue);
}

.btn a{
  text-decoration: none;
  font-weight: 600;
  font-size: 18px;
  color: black;
  font-family: primaryFont;
  
}

@keyframes fadeIn {
  0%{
    opacity: 0;
  }
  100%{
    opacity: 1;
  }
}
</style>
