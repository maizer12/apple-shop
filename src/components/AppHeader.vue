<template>
	<header class="header">
		<nav class="menu">
			<ul class="menu__items container">
				<li v-for="item in menu" :key="item.name" class="menu__item">
					<a href="/" class="menu__link">{{ item.name }}</a>
				</li>
			</ul>
		</nav>
		<div class="header__content container">
			<a href="#" class="logo">
				<img src="@/assets/img/logo.svg" alt="logo" class="logo__img" />
			</a>
			<app-search />
			<div class="header__right">
				<a href="tel:380978985931" class="header__tell">
					<svg
						width="17"
						height="17"
						viewBox="0 0 17 17"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							fill-rule="evenodd"
							clip-rule="evenodd"
							d="M0 2.62472C0 1.99957 0.248341 1.40002 0.690391 0.957969C1.13244 0.515919 1.73199 0.267578 2.35714 0.267578H3.43514C4.11086 0.267578 4.70014 0.728007 4.86436 1.38329L5.73257 4.85851C5.80293 5.13979 5.78872 5.43558 5.69172 5.70882C5.59472 5.98207 5.41925 6.22061 5.18729 6.39458L4.17136 7.15672C4.06529 7.23608 4.0425 7.35236 4.07236 7.43329C4.5158 8.63925 5.21604 9.73442 6.1246 10.643C7.03316 11.5515 8.12833 12.2518 9.33429 12.6952C9.41521 12.7251 9.53071 12.7023 9.61086 12.5962L10.373 11.5803C10.547 11.3483 10.7855 11.1729 11.0588 11.0759C11.332 10.9789 11.6278 10.9647 11.9091 11.035L15.3843 11.9032C16.0396 12.0674 16.5 12.6567 16.5 13.3332V14.4104C16.5 15.0356 16.2517 15.6351 15.8096 16.0772C15.3676 16.5192 14.768 16.7676 14.1429 16.7676H12.375C5.54086 16.7676 0 11.2267 0 4.39258V2.62472Z"
							fill="#3E4D31"
						/>
					</svg>

					+380 (97) 898-59-31</a
				>
				<div class="header__favorite">
					<span class="header__favorite-num">0</span>
					<svg
						width="22"
						height="20"
						viewBox="0 0 22 20"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
					>
						<path
							d="M10.5995 19.9006L10.5916 19.8973L10.5668 19.8839C10.4216 19.8052 10.2775 19.7245 10.1347 19.6417C8.41733 18.6367 6.81241 17.456 5.34656 16.1194C2.75056 13.7338 0 10.1937 0 5.83356C0 2.58014 2.7799 7.88367e-05 6.13518 7.88367e-05C7.06793 -0.00442064 7.9897 0.19824 8.83195 0.592989C9.6742 0.987737 10.4153 1.56442 11 2.28014C11.5849 1.56427 12.3261 0.987502 13.1686 0.592747C14.011 0.197992 14.933 -0.00458795 15.8659 7.88367e-05C19.2201 7.88367e-05 22 2.58014 22 5.83356C22 10.1948 19.2494 13.7349 16.6534 16.1183C15.1876 17.4549 13.5827 18.6356 11.8653 19.6406C11.7225 19.7237 11.5784 19.8049 11.4332 19.8839L11.4084 19.8973L11.4005 19.9017L11.3971 19.9028C11.2748 19.9666 11.1384 20 11 20C10.8616 20 10.7252 19.9666 10.6029 19.9028L10.5995 19.9006Z"
							fill="#3E4D31"
						/>
					</svg>
				</div>
				<main-button>Каталог</main-button>
			</div>
		</div>
	</header>
</template>

<script>
import { headerMenu } from '@/_config'
import AppSearch from './AppSearch.vue'
import MainButton from './ui/buttons/MainButton.vue'
export default {
	components: { AppSearch, MainButton },
	data() {
		return {
			menu: headerMenu,
		}
	},
}
</script>

<style lang="scss" scoped>
.menu {
	background-color: #5b5729;
	padding: 10px 0;
	&__items {
		display: flex;
		justify-content: end;
		column-gap: 45px;
	}
	&__link {
		color: #fff;
		font-family: Manrope;
		font-size: 12px;
		font-weight: 500;
		line-height: 1.333;
		letter-spacing: 0em;
		text-align: left;
		transition: 0.5s;
		position: relative;
		&:after {
			content: '';
			position: absolute;
			background-color: #fff;
			width: 0;
			height: 1px;
			bottom: 0;
			left: 0;
			transition: 0.4s;
		}
		&:hover {
			&:after {
				width: 100%;
			}
		}
	}
}
</style>
