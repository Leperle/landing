<!--suppress HtmlUnknownAttribute -->
<template>
	<header>
		<div :class="`${this.fullwidth ? 'lg:px-20 py-10' : 'mx-auto max-w-7xl py-10 px-5'} flex justify-center lg:justify-between`">
			<div>
				<div class="flex items-center justify-between w-full md:w-auto">
					<NuxtLink class="flex-shrink-0 flex items-center" to="/">
						<Logo class="h-10 mr-2" />
						<h1 class="text-2xl font-extrabold leading-7 ml-2">Parasol <span class="">Finance</span></h1>
					</NuxtLink>
				</div>
			</div>
			<div class="hidden space-x-10 md:flex items-center md:ml-10">
				<NuxtLink :to="{path: '/', hash: 'features'}" v-scroll-to="{el: '#features'}" class="font-medium text-white hover:text-gray-300">
					About Parasol Finance
				</NuxtLink>
				<NuxtLink :to="{path: '/', hash: 'roadmap'}" exact-active-class="active" v-scroll-to="{el: '#roadmap'}" class="font-medium nav-link text-white hover:text-gray-300">
					Roadmap
				</NuxtLink>
				<a href="https://docs.parasol.finance" target="_blank" class="font-medium nav-link text-white hover:text-gray-300">
					Read Docs.
				</a>
				<a href="https://forms.gle/jypcaJgvPgrkYmRDA" class="font-medium text-white nav-link hover:text-gray-300">
					Apply for IDO
				</a>
				<a href="https://app.parasol.finance/" class="items-center px-4 flex py-2 shadow-xl bg-gradient-primary text-sm font-medium rounded-full text-white">
					<svg class="w-6 h-6 mr-1" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path d="M11 3a1 1 0 100 2h2.586l-6.293 6.293a1 1 0 101.414 1.414L15 6.414V9a1 1 0 102 0V4a1 1 0 00-1-1h-5z"></path><path d="M5 5a2 2 0 00-2 2v8a2 2 0 002 2h8a2 2 0 002-2v-3a1 1 0 10-2 0v3H5V7h3a1 1 0 000-2H5z"></path></svg>
					Open Application
				</a>
			</div>
		</div>
	</header>
</template>

<script>
export default {
	name: "Header",
	props: {
		fullwidth: Boolean
	}
}
</script>

<style scoped>
.full
{
	//background: #1d1520;
	//padding: 1.75rem 5rem;
	//box-shadow: 0 0 3rem #00000038;
}
.nav-link {
	display: inline-block;
	position: relative;
	//color: #0087ca;
}

.nav-link:after {
	content: '';
	position: absolute;
	width: 100%;
	transform: scaleX(0);
	height: 2px;
	bottom: -5px;
	left: 0;
	background-color: white;
	transform-origin: bottom right;
	transition: transform 0.25s ease-out;
}

.nav-link:hover:after, .nav-link.active:after {
	transform: scaleX(1);
	transform-origin: bottom left;
}
</style>
