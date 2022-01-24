<template>
	<article
		@mouseenter="play"
		@mouseleave="pause"
		class="flex mx-4 lg:mx-0 flex-col rounded-xl shadow-lg scale-125 bg-white bg-opacity-5 text-white overflow-hidden">
		<div class="p-5">
			<video ref="preview" loop class="w-full rounded-lg mb-6">
				<source :src="video" />
			</video>
			<div class="px-4 py-1">
				<div>
					<h3
						class="inline-flex mt-2 px-4 py-1 rounded-full text-sm font-semibold tracking-wide uppercase bg-white text-gray-800">
						{{ name }}
					</h3>
				</div>
				<div class="mt-4 flex items-baseline text-5xl xl:text-5xl lg:text-3xl font-extrabold">
					<span v-if="earlyInvestor" class="text-transparent bg-clip-text bg-gradient-primary">
						{{ (price / 1.05).toLocaleString('en-US', { minimumFractionDigits: 0 }) }}
					</span>
					<span v-else class="text-white">
						{{ price.toLocaleString('en-US', { minimumFractionDigits: 0 }) }}
					</span>
					<span class="ml-1 text-2xl font-medium text-gray-200">PSOL</span>
				</div>
				<p v-if="earlyInvestor" class="text-lg font-bold text-gray-200">
					Reduced price of {{ price.toLocaleString('en-US', { minimumFractionDigits: 0 }) }} PSOL
				</p>
				<p class="mt-5 text-lg text-gray-200">
					Guaranteed allocation of <span class="font-extrabold text-purple-500">the amount of {{ price.toLocaleString('en-US', { minimumFractionDigits: 0 }) }} PSOL in dollars</span>
					at the time of the participation.
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
						Guaranteed allocation
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
						<span class="font-bold">Dynamic Vesting Period:</span> {{ vestingPeriod }} weeks
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
						<span class="font-bold">Starting Vesting Fees:</span> {{ vestingFees }}%
					</p>
				</li>
			</ul>
			<div class="rounded-md shadow">
				<OrderButton :amount="price"/>
			</div>
		</div>
	</article>
</template>

<script>
export default {
	name: "NftCard",
	props: {
		video: String,
		name: String,
		price: Number,
		vestingPeriod: Number,
		vestingFees: Number,
		earlyInvestor: Boolean
	},
	methods: {
		play() {
			this.$refs.preview.play();
		},
		pause() {
			this.$refs.preview.pause();
		}
	}
}
</script>

<style scoped>
article
{
	cursor: pointer;
	transition: transform .7s ease;
}

article:hover
{
	//box-shadow: 0 0 2.1rem #7939FF;
	//zoom: 1.1;
	transform: scale(1.021);
	//transform: translateY(-0.5rem);
}

article:hover video
{
}
</style>
