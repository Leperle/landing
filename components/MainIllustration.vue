<template>
	<div class="w-full relative">
		<img class="absolute w-full img_logo" alt="l" src="~/assets/images/Logo.png" />
		<img class="absolute w-full img_psol" alt="l" src="~/assets/images/Logo_P.png" />
		<img class="absolute w-full img_token" alt="l" src="~/assets/images/Logo_Q_.png" />
 	</div>
</template>
<script>
export default {
	name: "MainIllustration"
}
</script>

<style scoped>
div
{
	margin: -50px -100px 0px 0px;
    position: relative;
}

.img_logo
{
	animation: logo 15s linear infinite;
	z-index:1;
}

.img_psol
{
	animation: psol 20s linear infinite;
	z-index:0;
}

.img_token
{
	animation: token 15s linear infinite;
	z-index:2;
}


@keyframes logo {
  0% {
    transform: rotate(0deg) translateY(-20px) rotate(0deg) scale(1);
    filter: brightness(100%);
  }
  50% {
    transform: rotate(0deg) translateY(-10px) rotate(0deg) scale(1);
    filter: brightness(110%);
  }
  100% {
    transform: rotate(0deg) translateY(-20px) rotate(0deg) scale(1);
    filter: brightness(100%);
  }
}

@keyframes psol {
  0% {
    transform: rotate(0deg) translateX(5px) rotate(0deg) scale(0.95);
    filter: blur(1px);
  }
  50% {
    transform: rotate(180deg) translateX(10px) rotate(-180deg) scale(1);
    filter: blur(1px);
  }
  100% {
    transform: rotate(360deg) translateX(5px) rotate(-360deg) scale(0.95);
    filter: blur(1px);
  }
}

@keyframes token {
  0% {
    transform: rotate(0deg) translateX(5px) rotate(0deg) scale(0.95);
    filter: brightness(100%);
  }
  50% {
    transform: rotate(180deg) translateX(10px) rotate(-180deg) scale(1);
    filter: brightness(110%);
  }
  100% {
    transform: rotate(360deg) translateX(5px) rotate(-360deg) scale(0.95);
    filter: brightness(100%);
  }
}

</style>
