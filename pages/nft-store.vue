<template>
	<section v-if="preview" class="">
		<div class="pt-12">
			<div class="max-w-7xl mx-auto text-center px-4 sm:px-6 lg:px-8">
				<div class="max-w-3xl mx-auto space-y-2 lg:max-w-none">
					<p class="text-3xl font-extrabold text-white sm:text-4xl lg:text-5xl">
						Choose Your NFT Access Key
					</p>
					<p class="text-xl text-gray-300">
						Pre-Order your NFT Access Key using $PSOL token.
						<a class="text-purple-500" target="_blank" href="https://medium.com/@parasol-finance/parasol-finance-nfts-as-tiers-4dcfd48ca7e">Read More</a>
					</p>
				</div>
			</div>
		</div>
		<div class="relative mt-8 pb-12 sm:mt-12 sm:pb-16 lg:mt-16 lg:pb-24 text-gray-700">
			<div class="relative">
				<div class="relative z-10 max--w-7xl mx-auto">
					<div class="mx-auto space-y-4 lg:max-w-12xl- lg:px-20 lg:grid lg:grid-cols-4 lg:gap-5 lg:space-y-0">
						<div
							class="flex mx-4 lg:mx-0 flex-col rounded-xl shadow-lg scale-125 bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video ref="tiers1" autoplay loop class="w-full rounded-lg mb-6">
									<source src="~/assets/videos/1.mp4" />
								</video>
								<div class="px-4 py-1">
									<div>
										<h3
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Dreamer
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-5xl xl:text-5xl lg:text-3xl font-extrabold">
										210
										<span class="ml-1 text-2xl font-medium text-gray-200">PSOL</span>
									</div>
									<p class="mt-5 text-lg text-gray-200">
										Guaranteed Allocation of <span class="font-extrabold text-purple-500">the amount of 210 PSOL in dollars</span> at the time of the participation.
									</p>
								</div>
							</div>
							<div class="flex-1 flex flex-col justify-between px-8 pb-8 space-y-6">
								<ul class="space-y-4" role="list">
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 font-bold text-base text-gray-200">
											Guaranteed Allocation
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Dynamic Vesting Period:</span> 12 weeks
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Starting Vesting Fees:</span> 21%
										</p>
									</li>
								</ul>
								<div class="rounded-md shadow">
									<OrderButton :amount="210"/>
								</div>
							</div>
						</div>
						<div
							class="flex mx-4 lg:mx-0 flex-col rounded-xl shadow-lg bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video autoplay loop class="w-full rounded-lg mb-6">
									<source src="~/assets/videos/2.mp4" />
								</video>
								<div class="px-4 py-1">
									<div>
										<h3 id="tier-standard"
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Rider
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-5xl xl:text-5xl lg:text-3xl font-extrabold">
										2,100
										<span class="ml-1 text-2xl font-medium text-gray-200">
											PSOL
										</span>
									</div>
									<p class="mt-5 text-lg text-gray-200">
										Guaranteed Allocation of <span class="font-extrabold text-purple-500">the amount of 2,100 PSOL in dollars</span> at the time of the participation.
									</p>
								</div>
							</div>
							<div class="flex-1 flex flex-col justify-between px-8 pb-8 space-y-6">
								<ul class="space-y-4" role="list">
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 font-bold text-base text-gray-200">
											Guaranteed Allocation
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Dynamic Vesting Period:</span> 8 weeks
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Starting Vesting Fees:</span> 21%
										</p>
									</li>
								</ul>
								<div class="rounded-md shadow">
									<OrderButton :amount="2100"/>
								</div>
							</div>
						</div>
						<div
							class="flex mx-4 lg:mx-0 flex-col rounded-xl shadow-lg bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video autoplay loop class="w-full rounded-lg mb-6">
									<source src="~/assets/videos/3.mp4" />
								</video>
								<div class="px-4 py-1">
									<div>
										<h3
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Chiller
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-5xl xl:text-5xl lg:text-3xl font-extrabold">
										21,000
										<span class="ml-1 text-2xl font-medium text-gray-200">PSOL</span>
									</div>
									<p class="mt-5 text-lg text-gray-200">
										Guaranteed Allocation of <span class="font-extrabold text-purple-500">the amount of 21,000 PSOL in dollars</span> at the time of the participation.
									</p>
								</div>
							</div>
							<div class="flex-1 flex flex-col justify-between px-8 pb-8 space-y-6">
								<ul class="space-y-4" role="list">
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 font-bold text-base text-gray-200">
											Guaranteed Allocation
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Dynamic Vesting Period:</span> 6 weeks
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Starting Vesting Fees:</span> 21%
										</p>
									</li>
								</ul>
								<div class="rounded-md shadow">
									<OrderButton :amount="21000"/>
								</div>
							</div>
						</div>
						<div
							class="flex mx-4 lg:mx-0 flex-col rounded-xl shadow-lg bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video autoplay loop class="w-full rounded-lg mb-6">
									<source src="~/assets/videos/4.mp4" />
								</video>
								<div class="px-4 py-1">
									<div>
										<h3
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Moonwalker
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-5xl xl:text-5xl lg:text-3xl font-extrabold">
										210,000
										<span class="ml-1 text-2xl font-medium text-gray-200">PSOL</span>
									</div>
									<p class="mt-5 text-lg text-gray-200">
										Guaranteed Allocation of <span class="font-extrabold text-purple-500">the amount of 210,000 PSOL in dollars</span> at the time of the participation.
									</p>
								</div>
							</div>
							<div class="flex-1 flex flex-col justify-between px-8 pb-8 space-y-6">
								<ul class="space-y-4" role="list">
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 font-bold text-base text-gray-200">
											Guaranteed Allocation
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Dynamic Vesting Period:</span> 4 weeks
										</p>
									</li>
									<li class="flex items-start">
										<div class="flex-shrink-0">
											<svg aria-hidden="true" class="h-6 w-6 text-purple-500" fill="none"
												 stroke="currentColor" viewBox="0 0 24 24"
												 xmlns="http://www.w3.org/2000/svg">
												<path d="M5 13l4 4L19 7" stroke-linecap="round" stroke-linejoin="round"
													  stroke-width="2"/>
											</svg>
										</div>
										<p class="ml-3 text-base text-gray-200">
											<span class="font-bold">Starting Vesting Fees:</span> 21%
										</p>
									</li>
								</ul>
								<div class="rounded-md shadow">
									<OrderButton :amount="210000"/>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
	<section v-else class="countdown w-full flex flex-col gap-3 pb-12 items-center justify-center">
		<div class="hidden absolute inset-0 overflow-hidden rounded-3xl lg:block" style="z-index: -1;">
			<svg class="absolute bottom-full left-full transform translate-y-1/3 -translate-x-2/3 xl:bottom-auto xl:top-0 xl:translate-y-0" width="404" height="384" fill="none" viewBox="0 0 404 384" aria-hidden="true">
				<defs>
					<pattern id="64e643ad-2176-4f86-b3d7-f2c5da3b6a6d" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
						<rect x="0" y="0" width="4" height="4" class="text-indigo-900" fill="currentColor" />
					</pattern>
				</defs>
				<rect width="404" height="384" fill="url(#64e643ad-2176-4f86-b3d7-f2c5da3b6a6d)" />
			</svg>
			<svg class="absolute top-full transform -translate-y-1/3 -translate-x-1/3 xl:-translate-y-1/2" width="404" height="384" fill="none" viewBox="0 0 404 384" aria-hidden="true">
				<defs>
					<pattern id="64e643ad-2176-4f86-b3d7-f2c5da3b6a6d" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
						<rect x="0" y="0" width="4" height="4" class="text-indigo-900 text-opacity-60" fill="currentColor" />
					</pattern>
				</defs>
				<rect width="404" height="384" fill="url(#64e643ad-2176-4f86-b3d7-f2c5da3b6a6d)" />
			</svg>
		</div>
		<h1 class="text-5xl font-extrabold">
			<span
				class="text-transparent bg-clip-text bg-gradient-primary leading-normal whitespace-nowrap inline-block">
				Parasol Finance
			</span>
			<span class="text-white">| NFT Access Keys</span>
		</h1>
		<vue-countdown tag="div" class="flex gap-6 mb-3 justify-around items-center" :time="presaleTimeOffset" :interval="100" v-slot="{ days, hours, minutes, seconds, milliseconds }">
			<div class="flex flex-col text-center">
				<span class="text-9xl font-extrabold">{{ days }}</span>
				<span class="text-gray-200 text-xl text-center">Days</span>
			</div>
			<div class="text-9xl pt-3 font-extrabold text-gray-200 mb-12">:</div>
			<div class="flex flex-col">
				<span class="text-9xl font-extrabold">{{ hours }}</span>
				<span class="text-gray-200 text-xl text-center">Hours</span>
			</div>
			<div class="text-9xl pt-3 font-extrabold text-gray-200 mb-12">:</div>
			<div class="flex flex-col">
				<span class="text-9xl font-extrabold">{{ minutes }}</span>
				<span class="text-gray-200 text-xl text-center">Minutes</span>
			</div>
			<div class="text-9xl pt-3 font-extrabold text-gray-200 mb-12">:</div>
			<div class="flex flex-col">
				<span class="text-9xl font-extrabold">{{ seconds }}</span>
				<span class="text-gray-200 text-xl text-center">Seconds</span>
			</div>
		</vue-countdown>
		<p class="text-2xl font-light text-center">Parasol Finance is adopting a unique and never-before-seen<br />mechanism for our upcoming IDO launchpad.</p>
		<div class="mt-10 flex gap-5 justify-center items-center">
			<div class="rounded-md shadow">
				<button @click="preview = !preview" class="w-full flex items-center justify-center px-8 py-3 text-base font-medium rounded-full text-white text-white bg-gradient-primary hover:from-pink-600 hover:to-purple-500 md:py-4 md:text-lg md:px-10">
					<svg class="w-6 h-6 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
					Compare NFT Access Keys
				</button>
			</div>
			<div class="rounded-md shadow">
				<a href="https://medium.com/@parasol-finance/parasol-finance-nfts-as-tiers-4dcfd48ca7e" target="_blank" class="w-full flex items-center justify-center px-8 py-3 border border-white text-base font-medium rounded-full text-gray-200 hover:bg-white hover:text-gray-800 md:py-4 md:text-lg md:px-10">
					<svg class="w-6 h-6 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
					Read More About The Concept
				</a>
			</div>
		</div>
	</section>
</template>
<script>
export default {
	name: "nft-store",
	data() {
		return {
			preview: false,
			now: new Date(),
			presaleDate: new Date("Tue, 1 Feb 2022 21:00:21 GMT"),
			presaleTimeOffset: 0,
		}
	},
	mounted() {
		this.presaleTimeOffset = this.presaleDate - new Date();
		// this.$refs.tiers1.play();
	}
}
</script>

<style scoped>
section.countdown
{
	height: calc(100vh - 176px - 120px);
}
</style>
