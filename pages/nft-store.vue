<template>
	<section v-if="preview" class="">
		<div class="pt-12">
			<div class="max-w-7xl mx-auto text-center px-4 sm:px-6 lg:px-8">
				<div class="max-w-3xl mx-auto space-y-2 lg:max-w-none">
					<p class="text-3xl font-extrabold text-white sm:text-4xl lg:text-5xl">
						Choose Your NFT Access Key
					</p>
					<p class="text-xl text-gray-300">
						Ready to Buy your NFT Access Key using $PSOL token.
						<a class="text-purple-500" target="_blank"
						   href="https://medium.com/@parasol-finance/parasol-finance-nfts-as-tiers-4dcfd48ca7e">Read
							More.</a>
					</p>
					<NuxtLink to="/claim-bonus" class="flex justify-center items-center gap-2 text-3xl pt-6 font-extrabold text-purple-500">
						<svg class="w-7 h-7" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v13m0-13V6a2 2 0 112 2h-2zm0 0V5.5A2.5 2.5 0 109.5 8H12zm-7 4h14M5 12a2 2 0 110-4h14a2 2 0 110 4M5 12v7a2 2 0 002 2h10a2 2 0 002-2v-7"></path></svg>
						Early Investor? Claim Bonus!
					</NuxtLink>
<!--					<p class="text-gray-300 text-sm">If you hold PSOL since the beginning you might be eligible for a bonus!</p>-->
				</div>
			</div>
		</div>
		<div class="relative mt-3 pb-12 sm:mt-12 sm:pb-16 lg:mt-16 lg:pb-24 text-gray-700">
			<div class="relative">
				<div class="relative z-10 max--w-7xl mx-auto">
					<div class="mx-auto space-y-4 lg:max-w-12xl- lg:px-20 lg:grid lg:grid-cols-4 lg:gap-5 lg:space-y-0">
						<NftCard v-for="nft in nfts" :video="nft.video" :name="nft.name" :price="nft.price"
								 :vestingPeriod="nft.vestingPeriod"
								 :vestingFees="nft.vestingFees" :key="nft.name" :earlyInvestor="isEarlyInvestor()" />
					</div>
				</div>
			</div>
		</div>
	</section>
	<section v-else class="countdown w-full flex flex-col gap-3 pb-12 items-center justify-center">
		<div class="hidden absolute inset-0 overflow-hidden rounded-3xl lg:block" style="z-index: -1;">
			<svg
				class="absolute bottom-full left-full transform translate-y-1/3 -translate-x-2/3 xl:bottom-auto xl:top-0 xl:translate-y-0"
				width="404" height="384" fill="none" viewBox="0 0 404 384" aria-hidden="true">
				<defs>
					<pattern id="64e643ad-2176-4f86-b3d7-f2c5da3b6a6d" x="0" y="0" width="20" height="20"
							 patternUnits="userSpaceOnUse">
						<rect x="0" y="0" width="4" height="4" class="text-indigo-900" fill="currentColor"/>
					</pattern>
				</defs>
				<rect width="404" height="384" fill="url(#64e643ad-2176-4f86-b3d7-f2c5da3b6a6d)"/>
			</svg>
			<svg class="absolute top-full transform -translate-y-1/3 -translate-x-1/3 xl:-translate-y-1/2" width="404"
				 height="384" fill="none" viewBox="0 0 404 384" aria-hidden="true">
				<defs>
					<pattern id="64e643ad-2176-4f86-b3d7-f2c5da3b6a6d" x="0" y="0" width="20" height="20"
							 patternUnits="userSpaceOnUse">
						<rect x="0" y="0" width="4" height="4" class="text-indigo-900 text-opacity-60"
							  fill="currentColor"/>
					</pattern>
				</defs>
				<rect width="404" height="384" fill="url(#64e643ad-2176-4f86-b3d7-f2c5da3b6a6d)"/>
			</svg>
		</div>
		<h1 class="text-5xl font-extrabold">
			<span
				class="text-transparent bg-clip-text bg-gradient-primary leading-normal whitespace-nowrap inline-block">
				Parasol Finance
			</span>
			<span class="text-white">| NFT Access Keys</span>
		</h1>
		<vue-countdown tag="div" class="flex gap-6 mb-3 justify-around items-center" :time="presaleTimeOffset"
					   :interval="100" v-slot="{ days, hours, minutes, seconds, milliseconds }">
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
		<p class="text-2xl font-light text-center">Parasol Finance is adopting a unique and never-before-seen<br/>mechanism
			for our upcoming IDO launchpad.</p>
		<div class="mt-10 flex gap-5 justify-center items-center">
			<div class="rounded-md shadow">
				<button @click="play"
						class="w-full flex items-center justify-center px-8 py-3 text-base font-medium rounded-full text-white text-white bg-gradient-primary hover:from-pink-600 hover:to-purple-500 md:py-4 md:text-lg md:px-10">
					<svg class="w-6 h-6 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"
						 xmlns="http://www.w3.org/2000/svg">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
							  d="M3 3h2l.4 2M7 13h10l4-8H5.4M7 13L5.4 5M7 13l-2.293 2.293c-.63.63-.184 1.707.707 1.707H17m0 0a2 2 0 100 4 2 2 0 000-4zm-8 2a2 2 0 11-4 0 2 2 0 014 0z"></path>
					</svg>
					Compare NFT Access Keys
				</button>
			</div>
			<div class="rounded-md shadow">
				<a href="https://medium.com/@parasol-finance/parasol-finance-nfts-as-tiers-4dcfd48ca7e" target="_blank"
				   class="w-full flex items-center justify-center px-8 py-3 border border-white text-base font-medium rounded-full text-gray-200 hover:bg-white hover:text-gray-800 md:py-4 md:text-lg md:px-10">
					<svg class="w-6 h-6 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24"
						 xmlns="http://www.w3.org/2000/svg">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
							  d="M8.228 9c.549-1.165 2.03-2 3.772-2 2.21 0 4 1.343 4 3 0 1.4-1.278 2.575-3.006 2.907-.542.104-.994.54-.994 1.093m0 3h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
					</svg>
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
			participants: [],
			preview: true,
			now: new Date(),
			presaleDate: new Date("Tue, 1 Feb 2022 21:00:21 GMT"),
			presaleTimeOffset: 0,
			nfts: [
				{
					video: require('assets/videos/1.mp4'),
					name: 'Dreamer',
					price: 210,
					vestingPeriod: 12,
					vestingFees: 21
				},
				{
					video: require('assets/videos/2.mp4'),
					name: 'Rider',
					price: 2100,
					vestingPeriod: 8,
					vestingFees: 21
				},
				{
					video: require('assets/videos/3.mp4'),
					name: 'Chiller',
					price: 21000,
					vestingPeriod: 6,
					vestingFees: 21
				},
				{
					video: require('assets/videos/4.mp4'),
					name: 'MoonWalker',
					price: 210000,
					vestingPeriod: 4,
					vestingFees: 21
				}
			]
		}
	},
	mounted() {
		this.presaleTimeOffset = this.presaleDate - new Date();
		this.participants = require('assets/participants.json');
	},
	methods: {
		play() {
			this.preview = !this.preview;
		},
		isEarlyInvestor: function () {
			return this.$wallet.isConnected && this.participants.includes(this.$wallet.publicKey)
		},
	}
}
</script>

<style scoped>
section.countdown {
	height: calc(100vh - 176px - 120px);
}
</style>
