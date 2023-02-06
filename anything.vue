<template>
  <!-- <button @click="toggle">Toggle</button> -->
  <button @click="view('home')">Home</button>
  <button @click="view('counter')">Counter</button>

  <br/><hr/>
  <NuxtPage/>
  <br /><hr />
  <LazyHomeWelcome v-if="page === 'home'" />
  <LazyCounter v-if="page === 'counter'"/>
  <!-- <component :is="myComponent" /> -->
</template>

<script setup>
// const myComponent = shallowRef(resolveComponent('Counter'));
const myComponent = ref('counter');
const page = ref('test');
function toggle(){
  myComponent.value = 'welcome';
}

function view(name){
  page.value = name;
}
</script>