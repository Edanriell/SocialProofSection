<script lang="ts" setup></script>

<template>
	<main class="main-layout">
		<svg
			class="main-layout__wave-svg-sm"
			fill="none"
			height="232"
			preserveAspectRatio="none"
			viewBox="0 0 374 232"
			width="374"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				clip-rule="evenodd"
				d="M374 0C374 0 335.554 79.5975 228.536 100.66C121.518 121.722 162.03 142.966 109.453 185.126C56.8756 227.286 0 232 0 232V0H374Z"
				fill="url(#paint0_linear_0_4)"
				fill-rule="evenodd"
				opacity="0.05"
			/>
			<defs>
				<linearGradient
					id="paint0_linear_0_4"
					gradientUnits="userSpaceOnUse"
					x1="-180.212"
					x2="3.07959"
					y1="105.097"
					y2="419.392"
				>
					<stop stop-color="#8A4389" stop-opacity="0.01" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
				</linearGradient>
			</defs>
		</svg>
		<svg
			class="main-layout__wave-svg-lg"
			fill="none"
			height="362"
			preserveAspectRatio="none"
			viewBox="0 0 584 362"
			width="584"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				clip-rule="evenodd"
				d="M584 0C584 0 523.967 124.2 356.859 157.064C189.751 189.928 253.009 223.076 170.91 288.86C88.8111 354.645 0 362 0 362V0H584Z"
				fill="url(#paint0_linear_0_65)"
				fill-rule="evenodd"
				opacity="0.05"
			/>
			<defs>
				<linearGradient
					id="paint0_linear_0_65"
					gradientUnits="userSpaceOnUse"
					x1="-281.401"
					x2="4.4935"
					y1="163.987"
					y2="654.58"
				>
					<stop stop-color="#8A4389" stop-opacity="0.01" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
				</linearGradient>
			</defs>
		</svg>
		<slot />
		<svg
			class="main-layout__wave-wide-svg-sm"
			fill="none"
			height="673"
			preserveAspectRatio="none"
			viewBox="0 0 375 673"
			width="375"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				clip-rule="evenodd"
				d="M-355 673C-355 673 -243.466 442.099 67 381C377.466 319.901 259.94 258.276 412.47 135.975C565 13.6747 730 0 730 0V673H-355Z"
				fill="url(#paint0_linear_0_3)"
				fill-rule="evenodd"
				opacity="0.05"
			/>
			<defs>
				<linearGradient
					id="paint0_linear_0_3"
					gradientUnits="userSpaceOnUse"
					x1="1252.81"
					x2="721.123"
					y1="368.129"
					y2="-543.631"
				>
					<stop stop-color="#8A4389" stop-opacity="0.01" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
				</linearGradient>
			</defs>
		</svg>
		<svg
			class="main-layout__wave-wide-svg-lg"
			fill="none"
			height="673"
			preserveAspectRatio="none"
			viewBox="0 0 1085 673"
			width="1085"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				clip-rule="evenodd"
				d="M0 673C0 673 111.534 442.099 422 381C732.466 319.901 614.94 258.276 767.47 135.975C920 13.6747 1085 0 1085 0V673H0Z"
				fill="url(#paint0_linear_0_64)"
				fill-rule="evenodd"
				opacity="0.05"
			/>
			<defs>
				<linearGradient
					id="paint0_linear_0_64"
					gradientUnits="userSpaceOnUse"
					x1="1607.81"
					x2="1076.12"
					y1="368.129"
					y2="-543.631"
				>
					<stop stop-color="#8A4389" stop-opacity="0.01" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
					<stop offset="1" stop-color="#512051" />
				</linearGradient>
			</defs>
		</svg>
	</main>
</template>

<style scoped>
	.main-layout {
		position: relative;
		width: 100%;
		min-height: 100vh;
		overflow-x: hidden;
	}

	.main-layout__wave-svg-sm {
		position: absolute;
		display: block;
		top: 0;
		left: 0;
		width: 100vw;

		@media (width >= 1440px) {
			display: none;
		}
	}

	.main-layout__wave-wide-svg-sm {
		position: absolute;
		display: block;
		bottom: 0;
		left: 0;
		width: 100vw;

		@media (width >= 1440px) {
			display: none;
		}
	}

	.main-layout__wave-svg-lg {
		position: absolute;
		display: none;
		top: 0;
		left: 0;

		@media (width >= 1440px) {
			display: block;
		}
	}

	.main-layout__wave-wide-svg-lg {
		position: absolute;
		display: none;
		bottom: 0;
		right: 0;

		@media (width >= 1440px) {
			display: block;
		}
	}
</style>
