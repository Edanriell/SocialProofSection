<script lang="ts" setup>
	import { ReviewCard } from "@shared/ui/review-card";

	const reviewCardsData = [
		{
			rating: 5,
			text: "Rated 5 Stars in Reviews"
		},
		{
			rating: 5,
			text: "Rated 5 Stars in Report Guru"
		},
		{
			rating: 5,
			text: "Rated 5 Stars in BestTech"
		}
	];
</script>

<template>
	<section class="social-proof">
		<h1 class="visually-hidden">Social proof</h1>
		<div class="social-proof__text-content">
			<p
				class="social-proof__text social-proof__text--type--strong social-proof__text--size--large social-proof__text--color--murasaki"
			>
				10,000+ of our users love our products.
			</p>
			<p
				class="social-proof__text social-proof__text--type--normal social-proof__text--size--small social-proof__text--color--lepidolite-purple"
			>
				We only provide great products combined with excellent customer service. See what our
				satisfied customers are saying about our services.
			</p>
		</div>
		<ul class="social-proof__review-card-list">
			<li v-for="(reviewCard, index) in reviewCardsData" :key="index + '_' + reviewCard.text">
				<ReviewCard :stars="reviewCard.rating" :text="reviewCard.text" />
			</li>
		</ul>
		<ul></ul>
	</section>
</template>

<style scoped>
	.social-proof {
		position: relative;
		margin: 8.2rem 2.4rem 9.9rem 2.4rem;
		z-index: 2;
	}

	.social-proof__text-content {
		display: flex;
		flex-direction: column;
		row-gap: 1.7rem;
		margin-bottom: 3.9rem;
	}

	.social-proof__text {
		font-family: var(--font-family), sans-serif;
		text-align: center;
		margin: 0;
	}

	.social-proof__text--type--strong {
		font-weight: 700;
		line-height: 80%;
		letter-spacing: -0.04em;
	}

	.social-proof__text--type--normal {
		font-weight: 500;
		line-height: 132%;
		letter-spacing: -0.03em;
	}

	.social-proof__text--size--small {
		font-size: 1.9rem;
	}

	.social-proof__text--size--large {
		font-size: 4rem;
	}

	.social-proof__text--color--lepidolite-purple {
		color: var(--lepidolite-purple);
	}

	.social-proof__text--color--murasaki {
		color: var(--murasaki);
	}

	.social-proof__review-card-list {
		list-style: none;
		padding: 0;
		margin: 0;
		display: flex;
		flex-direction: column;
		row-gap: 1.6rem;
		margin-bottom: 4.9rem;
	}
</style>
