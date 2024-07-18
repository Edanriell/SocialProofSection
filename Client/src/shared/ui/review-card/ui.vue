<script lang="ts" setup>
	const props = defineProps<{
		description: string;
		rating: number;
	}>();

	const maxRating = 5;
	const selectedStars = props.rating <= 0 ? 0 : props.rating <= maxRating ? props.rating : 5;
	const unselectedStars =
		props.rating <= 0 ? 5 : props.rating <= maxRating ? maxRating - props.rating : 0;
</script>

<template>
	<div class="review-card">
		<ol class="review-card__stars-list">
			<li
				v-for="(starValue, index) in selectedStars"
				:key="index + '-' + starValue"
				class="review-card__star"
			>
				<span class="visually-hidden">Star value {{ starValue }}</span>
				<svg
					class="review-card__star"
					fill="none"
					height="16"
					viewBox="0 0 17 16"
					width="17"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path
						d="M16.5386 6.00296C16.5036 5.8957 16.4109 5.81748 16.2992 5.80119L10.9392 5.02222L8.54216 0.165333C8.49238 0.064 8.38927 0 8.27668 0C8.16408 0 8.06068 0.064 8.01119 0.165333L5.61386 5.02252L0.253861 5.80148C0.142157 5.81778 0.049713 5.8957 0.0144538 6.00326C-0.0202129 6.11022 0.00852784 6.22815 0.0894167 6.30667L3.96823 10.0874L3.05238 15.4261C3.03342 15.5372 3.07905 15.6495 3.17001 15.7159C3.26156 15.7828 3.38275 15.7914 3.48201 15.7384L8.27668 13.2181L13.0708 15.7384C13.114 15.7612 13.1617 15.7724 13.2088 15.7724C13.2702 15.7724 13.3312 15.7535 13.383 15.7159C13.4743 15.6495 13.5199 15.5372 13.5007 15.4261L12.5851 10.0877L16.4639 6.30667C16.5445 6.22756 16.5736 6.10993 16.5386 6.00296Z"
						fill="var(--physalis)"
					/>
				</svg>
			</li>
			<li
				v-for="(starValue, index) in unselectedStars"
				:key="index + '-' + starValue"
				class="review-card__star"
			>
				<span class="visually-hidden">Star value {{ starValue }}</span>
				<svg
					class="review-card__star"
					fill="none"
					height="16"
					viewBox="0 0 17 16"
					width="17"
					xmlns="http://www.w3.org/2000/svg"
				>
					<path
						d="M16.5386 6.00296C16.5036 5.8957 16.4109 5.81748 16.2992 5.80119L10.9392 5.02222L8.54216 0.165333C8.49238 0.064 8.38927 0 8.27668 0C8.16408 0 8.06068 0.064 8.01119 0.165333L5.61386 5.02252L0.253861 5.80148C0.142157 5.81778 0.049713 5.8957 0.0144538 6.00326C-0.0202129 6.11022 0.00852784 6.22815 0.0894167 6.30667L3.96823 10.0874L3.05238 15.4261C3.03342 15.5372 3.07905 15.6495 3.17001 15.7159C3.26156 15.7828 3.38275 15.7914 3.48201 15.7384L8.27668 13.2181L13.0708 15.7384C13.114 15.7612 13.1617 15.7724 13.2088 15.7724C13.2702 15.7724 13.3312 15.7535 13.383 15.7159C13.4743 15.6495 13.5199 15.5372 13.5007 15.4261L12.5851 10.0877L16.4639 6.30667C16.5445 6.22756 16.5736 6.10993 16.5386 6.00296Z"
						fill="var(--australian-apricot)"
					/>
				</svg>
			</li>
		</ol>
		<strong class="review-card__text">{{ props.description }}</strong>
	</div>
</template>

<style scoped>
	.review-card {
		border-radius: 0.8rem;
		background: var(--abalone);
		width: 100%;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		row-gap: 1.523rem;
		padding: 1.6rem 0 1.5rem 0;

		@media (width >= 1440px) {
			flex-direction: row;
			align-content: flex-start;
			justify-content: flex-start;
			max-width: 44.5rem;
			column-gap: 3.245rem;
			padding: 2rem 3.2rem 2rem 3.2rem;
		}
	}

	.review-card__text {
		font-family: var(--font-family), sans-serif;
		font-weight: 700;
		font-size: 1.7rem;
		color: var(--murasaki);
	}

	.review-card__stars-list {
		list-style: none;
		display: flex;
		flex-direction: row;
		align-items: center;
		justify-content: center;
		padding: 0;
		column-gap: 0.845rem;
	}

	.review-card__star {
		width: 1.655rem;
		height: 1.577rem;
	}
</style>
