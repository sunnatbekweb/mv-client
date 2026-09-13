<script setup lang="ts">
import { Search } from '@lucide/vue'
</script>

<template>
	<header class="header">
		<div class="container flex items-center justify-between">
			<a
				href="/"
				class="logo"
			>
				M-flix
			</a>
			<nav class="nav">
				<ul class="nav__list">
					<li class="nav__list--item">
						<a
							href="#"
							class="nav__list--item-link"
						>
							Home
						</a>
					</li>
					<li class="nav__list--item">
						<a
							href="#"
							class="nav__list--item-link"
						>
							Movies
						</a>
					</li>
					<li class="nav__list--item">
						<a
							href="#"
							class="nav__list--item-link"
						>
							Serials
						</a>
					</li>
					<li class="nav__list--item">
						<a
							href="#"
							class="nav__list--item-link"
						>
							Categories
						</a>
					</li>
				</ul>
			</nav>
			<form class="search">
				<input
					type="search"
					placeholder="Films, Serials, Actors"
					class="search__input"
				/>
				<button class="search__button group">
					<Search
						:size="20"
						opacity="0.6"
						class="group-hover:opacity-100 transition-opacity duration-150"
					/>
				</button>
			</form>
		</div>
	</header>
</template>

<style lang="scss" scoped>
.header {
	height: 72px;
	display: flex;
	align-items: center;
	background-color: #141414;
	color: #ffffff;

	& .logo {
		font-weight: 700;
		font-size: 36px;
	}

	& .nav {
		&__list {
			display: flex;
			align-items: center;
			gap: 60px;

			&--item {
				&-link {
					opacity: 0.6;
					transition: opacity 0.15s ease;

					&:hover {
						opacity: 1;
					}
				}
			}
		}
	}

	& .search {
		display: flex;
		align-items: center;
		background-color: #ffffff26;
		border-radius: 8px;

		&__input {
			padding: 8px 0 8px 16px;

			&:focus {
				outline: none;
			}
		}

		&__button {
			height: 100%;
			padding: 0 16px;
			border-radius: 0 8px 8px 0;
		}
	}
}
</style>
