<script lang="ts" setup>
	import { UserReviewCard } from "@entities/users/ui/user-review-card";
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

	const userReviewsCardsData = [
		{
			fullName: "Colton Smith",
			userType: "Verified Buyer",
			userImageUrl: "images/users/colton-smith-image.jpg",
			reviewText:
				"We needed the same printed design as the one we had ordered a week prior. Not only did they find the original order, but we also received it in time. Excellent!"
		},
		{
			fullName: "Irene Roberts",
			userType: "Verified Buyer",
			userImageUrl: "images/users/irene-roberts-image.jpg",
			reviewText:
				"Customer service is always excellent and very quick turn around. Completely delighted with the simplicity of the purchase and the speed of delivery."
		},
		{
			fullName: "Anne Wallace",
			userType: "Verified Buyer",
			userImageUrl: "images/users/anne-wallace-image.jpg",
			reviewText:
				"Put an order with this company and can only praise them for the very high standard. Will definitely use them again and recommend them to everyone!"
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
			<li v-for="(reviewCard, index) in reviewCardsData" :key="index + '-' + reviewCard.text">
				<ReviewCard :description="reviewCard.text" :rating="reviewCard.rating" />
			</li>
		</ul>
		<ul class="social-proof__user-reviews-list">
			<li
				v-for="(userReview, index) in userReviewsCardsData"
				:key="index + '-' + userReview.fullName"
			>
				<UserReviewCard
					:fullName="userReview.fullName"
					:reviewText="userReview.reviewText"
					:userImageUrl="userReview.userImageUrl"
					:userType="userReview.userType"
				/>
			</li>
		</ul>
	</section>
</template>

<style scoped>
	.social-proof {
		position: relative;
		margin: 0 2.4rem 0 2.4rem;
		padding: 8.2rem 0 9.9rem 0;
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
		display: flex;
		flex-direction: column;
		row-gap: 1.6rem;
		margin: 0 0 4.9rem 0;
	}

	.social-proof__user-reviews-list {
		list-style: none;
		padding: 0;
		margin: 0;
		display: flex;
		flex-direction: column;
		row-gap: 1.6rem;
	}
</style>
