<template>
	<section class="">
		<div class="pt-12">
			<div class="max-w-7xl mx-auto text-center px-4 sm:px-6 lg:px-8">
				<div class="max-w-3xl mx-auto space-y-2 lg:max-w-none">
					<!--					<h2 class="text-lg leading-6 font-semibold text-gray-300 uppercase tracking-wider">-->
					<!--						Parasol Finance-->
					<!--					</h2>-->
					<p class="text-3xl font-extrabold text-white sm:text-4xl lg:text-5xl">
						Choose Your NFT Access Key
					</p>
					<p class="text-xl text-gray-300">
						Pre-Order your NFT Access Key using $PSOL token.
					</p>
				</div>
			</div>
		</div>
		<div class="relative mt-8 pb-12 sm:mt-12 sm:pb-16 lg:mt-16 lg:pb-24 text-gray-700">
			<!--			<div v-if="!this.$wallet.isConnected" class="backdrop-filter text-white z-30 backdrop-blur-smo px-10 text-center flex flex-col justify-center items-center absolute top-0 left-0 w-full h-full">-->
			<!--				<h1 class="text-3xl mb-3 font-semibold">Connection Required</h1>-->
			<!--				<p class="mb-5">Your wallet is currently not connected and we need it to authenticate you.</p>-->
			<!--				<ConnectWallet />-->
			<!--			</div>-->
			<div class="relative">
				<div class="relative z-10 max--w-7xl mx-auto">
					<div class="mx-auto space-y-4 lg:max-w-12xl- lg:px-20 lg:grid lg:grid-cols-4 lg:gap-5 lg:space-y-0">
						<div
							class="flex flex-col suce rounded-xl shadow-lg scale-125 bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video autoplay loop class="w-full rounded-lg mb-6">
									<source src="/1.mp4" />
								</video>
<!--								<img alt="tiers-" class="w-full rounded-lg mb-6" src="https://i.imgur.com/sY5qRPA.jpg "/>-->
								<div class="px-4 py-1">
									<div>
										<h3
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Dreamer
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-6xl font-extrabold">
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
							class="flex flex-col rounded-xl shadow-lg bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video autoplay loop class="w-full rounded-lg mb-6">
									<source src="/2.mp4" />
								</video>
<!--								<img alt="tiers-" class="w-full rounded-lg mb-6" src="https://i.imgur.com/jHZ7WtI.jpg"/>-->
								<div class="px-4 py-1">
									<div>
										<h3 id="tier-standard"
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Rider
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-6xl font-extrabold">
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
<!--									<a aria-describedby="tier-standard" class="flex items-center uppercase justify-center mt-5 px-5 py-3 text-base font-medium rounded-md bg-gradient-to-r from-purple-500 to-pink-600 text-white" href="#">-->
<!--										Buy It For 2,100 $PSOL-->
<!--									</a>-->
								</div>
							</div>
						</div>
						<div
							class="flex flex-col rounded-xl shadow-lg bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video autoplay loop class="w-full rounded-lg mb-6">
									<source src="/3.mp4" />
								</video>
<!--								<img alt="tiers-" class="w-full rounded-lg mb-6" src="https://i.imgur.com/5T4JDSc.jpg"/>-->
								<div class="px-4 py-1">
									<div>
										<h3
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Chiller
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-6xl font-extrabold">
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
<!--									<a aria-describedby="tier-standard" class="flex items-center uppercase justify-center mt-5 px-5 py-3 text-base font-medium rounded-md bg-gradient-to-r from-purple-500 to-pink-600 text-white" href="#">-->
<!--										Buy It For 21,000 $PSOL-->
<!--									</a>-->
								</div>
							</div>
						</div>
						<div
							class="flex flex-col rounded-xl shadow-lg bg-white bg-opacity-5 text-white overflow-hidden">
							<div class="p-5">
								<video autoplay loop class="w-full rounded-lg mb-6">
									<source src="/4.mp4" />
								</video>
<!--								<img alt="tiers-" class="w-full rounded-lg mb-6" src="https://i.imgur.com/ESYb2Jr.jpg"/>-->
								<div class="px-4 py-1">
									<div>
										<h3
											class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
											Moonwalker
										</h3>
									</div>
									<div class="mt-4 flex items-baseline text-6xl font-extrabold">
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
</template>
<script>
export default {
	name: "nft-store",
}
</script>

<style scoped>
video {
	object-fit: fill;
	height: 350px;
	width: 100%;
}

.suce:hover {
//background-color: red !important;
}

img {
	//filter: hue-rotate(13deg);
}
</style>
