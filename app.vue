<script setup lang="ts">
import { THEMES, useThemeStore } from './store/theme';
import 'assets/css/main.css';

const themeStore = useThemeStore();
</script>

<template>
	<div
		:data-theme="themeStore.theme.dark ? THEMES.DARK : THEMES.LIGHT"
		class="bg-gradient-to-r from-base-100 to-neutral"
	>
		<div class="flex flex-col max-w-8xl mx-auto pb-8 pl-8 pr-8 pt-4 min-h-screen justify-between">
			<Header />
			<NuxtPage />
			<NuxtLayout name="custom" />
		</div>
	</div>
</template>
