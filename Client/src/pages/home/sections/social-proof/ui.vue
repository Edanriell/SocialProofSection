<script lang="ts" setup></script>

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
		<ul></ul>
		<ul></ul>
	</section>
</template>

<style scoped>
	.social-proof {
		margin: 8.2rem 2.4rem 9.9rem 2.4rem;
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
</style>
