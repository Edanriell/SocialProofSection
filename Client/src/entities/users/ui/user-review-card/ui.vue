<script lang="ts" setup>
	const props = defineProps<{
		fullName: string;
		userType: string;
		userImageUrl: string;
		reviewText: string;
	}>();
</script>

<template>
	<figure class="user-review-card">
		<figcaption class="user-review-card__user-info user-info">
			<picture>
				<source :srcset="props.userImageUrl" media="(min-width: 375px)" type="image/jpg" />
				<img :src="props.userImageUrl" alt="Image of Colton Smith" class="user-info__user-image" />
			</picture>
			<div class="user-info__text-content">
				<strong class="user-info__user-full-name">{{ props.fullName }}</strong>
				<p class="user-info__user-type">{{ props.userType }}</p>
			</div>
		</figcaption>
		<blockquote class="user-review-card__review-text">“ {{ props.reviewText }} ”</blockquote>
	</figure>
</template>

<style scoped>
	.user-review-card {
		border-radius: 0.8rem;
		background-color: var(--murasaki);
		padding: 4rem 3.2rem 3.5rem 3.2rem;
		width: 100%;
		margin: 0;

		@media (width >= 1440px) {
			max-width: 35rem;
		}
	}

	.user-review-card__user-info {
		position: relative;
	}

	.user-info {
		display: flex;
		flex-direction: row;
		column-gap: 2.3rem;
		align-items: center;
		justify-content: flex-start;
		margin-bottom: 2.3rem;

		@media (width >= 1440px) {
			margin-bottom: 3.1rem;
		}
	}

	.user-info__user-image {
		width: 4rem;
		height: 4rem;
		border-radius: 100%;
		object-fit: cover;
	}

	.user-info__text-content {
		display: block;
	}

	.user-info__user-full-name {
		font-family: var(--font-family), sans-serif;
		font-weight: 700;
		font-size: 1.7rem;
		color: var(--white);
		line-height: 0%;
	}

	.user-info__user-type {
		font-family: var(--font-family), sans-serif;
		font-weight: 400;
		font-size: 1.7rem;
		color: var(--fugitive-flamingo);
		line-height: 0%;
		margin: 1.3rem 0 0 0;
	}

	.user-review-card__review-text {
		font-family: var(--font-family), sans-serif;
		font-weight: 500;
		font-size: 1.7rem;
		line-height: 129%;
		letter-spacing: -0.02em;
		color: var(--white);
		margin: 0;
	}
</style>
