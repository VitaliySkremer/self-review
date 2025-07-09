<template>
	<div class="container">
    <div class="heading">
			<span>
				Self Review
			</span>
			<span class="heading__slot">
				/ <slot name="heading" />
			</span>
		</div>
		<div class="main">
			<slot name="default"/>
		</div>
		<img class="logo" src="/public/logos/1221.png">
		<div class="lines">
			<div class="line line-1"/>
			<div class="line line-2"/>
			<div class="line line-3"/>
		</div>
  </div>
</template>

<style scoped>
.container {
  height: 100%;
	width: 100%;
	padding: 40px;

	display: flex;
	flex-direction: column;

	position: relative;
}

.main {
	display: flex;
	flex: 1 1 auto;
}

.logo {


	width: 100px;
	height: 25px;


}

.heading {
	font-size: 20px;
	display: flex;
	flex-direction: column;
}

.heading__slot {
	color: #65CE1E;
}

.lines {
	position: absolute;
	top: 0;
	right: 0;
	height: 8px;
	width: 60%;
	display: flex;
}

.line {
	width: 100%;
	height: 100%;
}

.line-1 {
	background-color: #65CE1E;
}

.line-2 {
	background-color: #A3E278;
}

.line-3 {
	background-color: #C1EBA5;
}
</style>
