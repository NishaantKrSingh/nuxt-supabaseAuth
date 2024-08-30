<script setup>
const login_to = ()=> {
    return navigateTo('/login')
}
</script>

<template>
    <div>
        <div class="for-button">
            <button type="button" @click="login_to">Login</button>
        </div>
        <div>
            <h2 class="rotate">Index</h2>
            <h2>Page</h2>
        </div>
    </div>
</template>

<style lang="css" scoped>
div {
  font-family: "didot";
}

h2 {
  font-size: 100px;
  margin: 0;
   writing-mode: vertical-lr;
  text-align: center;
  line-height: .9;
}

.rotate {
   transform: rotate(180deg);
}

div {
  display: grid;
  height: 100vh;
  justify-content: center;
  align-content: center;
  grid-template-columns: max-content max-content;
}

body {
  margin: 0;
}

.for-button {
    position: relative;
    flex: 1;
}
button {
    position: fixed;
    cursor: pointer;
    top: 15px;
    right: 15px;
    border: none;
    border-radius: 12px;
    background-color: rgba(104, 85, 224, 1);
    color: white;
    padding: 13px 30px;
    font-size: 18px;
    transition-duration: 0.4s;
}
button:hover {
    border: 1px solid  rgba(104, 85, 224, 1);
    background-color: white;
    color:  rgba(104, 85, 224, 1);
}
</style>