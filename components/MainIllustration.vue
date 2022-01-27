<template>
	<div class="w-full relative">
		<img class="absolute w-full bounce1" alt="l" src="~/assets/images/Logo.png" />
		<img class="absolute w-full bounce2 spin" alt="l" src="~/assets/images/Logo_P.png" />
		<img class="absolute w-full bounce3 spin2" alt="l" src="~/assets/images/Logo_Q.png" />
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
	margin-top: -30px;
}

.bounce1
{
	animation: float 15s ease-in-out infinite;
}

.bounce2
{
	animation: float2 5s ease-in-out infinite;
}

.bounce3
{
	animation: float3 10s ease-in-out infinite;
}

.spin
{
	animation: spin 421s linear infinite;
}

.spin2
{
	animation: spin 421s linear infinite;
	animation-delay: 2s;
}

@keyframes float {
	0% {
		transform: translatey(0px);
	}

	50% {
		transform: translatey(-1rem);
	}

	100% {
		transform: translatey(0px);
	}
}

@keyframes float2 {
	0% {
		transform: translatey(-10px);
	}

	50% {
		transform: translatey(0);
	}

	100% {
		transform: translatey(-10px);
	}
}

@keyframes float3 {
	0% {
		transform: translatey(10px);
	}

	50% {
		transform: translatey(0);
	}

	100% {
		transform: translatey(10px);
	}
}

@keyframes spin {
	0% {
		transform: rotate(0);
	}

	100% {
		transform: rotate(360deg);
	}
}

</style>
