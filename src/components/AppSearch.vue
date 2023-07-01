<template>
	<div class="search">
		<input type="text" placeholder="Поиск" class="search__input" />
		<main-button>
			<img src="@/assets/img/search.svg" alt="search" />
			Пошук</main-button
		>
	</div>
</template>

<script>
import MainButton from './ui/buttons/MainButton.vue'
export default {
	components: { MainButton },
}
</script>

<style lang="scss" scoped>
.search {
	height: fit-content;
	display: flex;
	&__input {
		border: 1px solid #dddddd;
		padding: 9px 20px;
		color: rgba(0, 0, 0, 0.6);
		font-size: 13px;
		font-family: Manrope;
		font-style: normal;
		font-weight: 500;
		line-height: normal;
		width: 400px;
		display: block;
		&::placeholder {
			transition: 0.6s;
		}
		&:focus {
			&::placeholder {
				opacity: 0;
			}
		}
	}
}
</style>
