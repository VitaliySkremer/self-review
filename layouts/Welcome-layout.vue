<template>
	<div class="container">
    <div class="content">
      <slot />
    </div>
    <div class="comp">
      <img src="/public/logos/comp.png"/>
    </div>
  </div>
</template>

<style scoped>
.container {
  height: 100%;
  background-image: url('/public/БГ.png');
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
}

.comp {
  position: absolute;
  bottom: 0;
  padding: 40px;
}

.content {
  position: absolute;
  top: 40%;
  left: 70%;
  transform: translate(-50%, -50%);
  text-align: center;
}
</style>
