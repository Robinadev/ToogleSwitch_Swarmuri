<template>
    <div class="toggle-switch">
      <label>
        <input type="checkbox" v-model="isChecked" />
        <span class="slider"></span>
      </label>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isChecked = ref(false);
  </script>
  
  <style scoped>
  .toggle-switch {
    display: inline-block;
    position: relative;
  }
  
  input[type="checkbox"] {
    display: none;
  }
  
  .slider {
    display: inline-block;
    width: 50px;
    height: 25px;
    background: #ccc;
    border-radius: 15px;
    position: relative;
    cursor: pointer;
  }
  
  .slider:before {
    content: '';
    position: absolute;
    width: 20px;
    height: 20px;
    background: #fff;
    border-radius: 50%;
    top: 50%;
    left: 5px;
    transform: translateY(-50%);
    transition: 0.3s;
  }
  
  input[type="checkbox"]:checked + .slider {
    background: #42b983;
  }
  
  input[type="checkbox"]:checked + .slider:before {
    left: 25px;
  }
  </style>
  