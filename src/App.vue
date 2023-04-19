<template>
  <div id="app">
    <router-view />
  </div>
</template>

<style>

:root {
  --primary-color: #F30168;
  --primary-color-hover: #f83087;
}

* {
  margin: 0;
  padding: 0;
  margin: 0 auto;
  box-sizing: border-box;
}

body {
  background-color: #FAFAFC;
  font-family: 'Sora', sans-serif;
  font-size: 16px;
  width: 100%;
  height: 100vh;
  color: #292D32;
}

img {
  display: block;
}

button {
  text-transform: uppercase;
  font-size: 1rem ;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}

input {
  display: block;
  width: 100%;
  padding: 30px 16px;
  border: solid 1px rgba(81, 93, 116, 0.5);;
  border-radius: 5px;
  font-size: 1.25rem;
}

input::placeholder {
  font-size: 1rem;
  color: #292D32;
}

label {
  font-size: 1rem;
}

span {
  display: block;
}

h3 {
  font-size: 1.75rem;
  font-weight: bold;
  margin-bottom: 5x;
}

.primary-button {
  background-color: var(--primary-color);
  color: #fff;
  width: 100%;
  padding: 30px;
  transition: all 300ms ease;
}

.primary-button:hover {
  background-color: var(--primary-color-hover);
}

.primary-button:disabled {
  filter: opacity(30%);
  cursor: auto;
}



</style>
