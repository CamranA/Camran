<script lang="ts">
	import "./layout.css";
	import favicon from "$lib/assets/flame.svg";
	import * as NavigationMenu from "$lib/components/ui/navigation-menu/index.js";
	import { Flame, Braces } from "@lucide/svelte";
	let { children } = $props();
</script>

<svelte:head>
	<title>Camran Ahmad</title>
	<meta charset="UTF-8" />
	<meta name="description" content="Personal website of Camran Ahmad" />
	<meta name="keywords" content="HTML, CSS, JavaScript" />
	<meta name="author" content="Camran Ahmad" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
	<link rel="icon" style="color:red;" href={favicon} />
</svelte:head>

<!--
    STEP-BY-STEP GRID INSTRUCTIONS:
    1. Define a container (div.app-shell) to hold the layout.
    2. Use 'display: grid' to enable grid layout.
    3. Define 'grid-template-areas' to map out your layout visually.
    4. Assign grid areas to child elements using 'grid-area'.
    5. Use media queries to change the grid definition for different screen sizes.
-->

<div
	class="app-shell"
	style="opacity: 0.8; background-image: radial-gradient(rgba(51, 51, 51, 0.565) 0.5px, rgba(0, 0, 0, 0) 0.5px); background-size: 19px 19px; background-repeat: repeat;"
>
	<header class="header">
		<div class="header-content">
			<a class="main-icon" aria-label="Home" href="./"
				><Flame class="w-16 h-16"></Flame></a
			>
			<NavigationMenu.Root>
				<NavigationMenu.List>
					<NavigationMenu.Item>
						<NavigationMenu.Link
							class="text-lg"
							aria-label="Home"
							href="./">Home</NavigationMenu.Link
						>
					</NavigationMenu.Item>
					<NavigationMenu.Item>
						<NavigationMenu.Link
							class="text-lg"
							aria-label="Resume"
							href="./resume">Resume</NavigationMenu.Link
						>
					</NavigationMenu.Item>
				</NavigationMenu.List>
			</NavigationMenu.Root>
		</div>
	</header>

	<main class="main">
		{@render children()}
	</main>

	<footer class="footer bg-secondary text-secondary-foreground">
		<div class="footer-content">
			<a
				class="main-icon"
				href="https://github.com/CamranA/"
				target="_blank"
				aria-label="GitHub"
			>
				<Braces class="w-8 h-8"></Braces>
			</a>
		</div>
	</footer>
</div>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family:
			system-ui,
			-apple-system,
			sans-serif;
	}

	.main-icon {
		transition: color 0.3s ease;
	}
	.main-icon:hover {
		color: oklch(0.71 0.04 257); /* Color on hover */
	}

	.app-shell {
		display: grid;
		min-height: 100vh;
		/* Mobile-first: Single column layout */
		grid-template-columns: 1fr;
		grid-template-rows: auto 1fr auto;
		grid-template-areas:
			"header"
			"main"
			"footer";
		gap: 1rem;
		/* Smooth transition for layout changes */
		transition: all 0.3s ease;
	}

	.header {
		grid-area: header;
		background-color: var(--popover); /* Slightly transparent */
		opacity: 0.95;
		backdrop-filter: blur(5px); /* Blur effect for better readability */
		position: sticky;
		top: 0;
		z-index: 100; /* Ensure it stays on top */
		padding: 1rem;
		border-bottom: 1px solid #ddd;
		display: flex;
		justify-content: center; /* Center the content wrapper */
	}

	.footer {
		display: flex;
		justify-content: center; /* Center the content wrapper */
	}

	.header-content {
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		max-width: 1024px; /* Match the main content max-width */
	}

	.footer-content {
		display: flex;
		justify-content: space-between;
		align-items: center;
		width: 100%;
		max-width: 1024px; /* Match the main content max-width */
	}

	.main {
		grid-area: main;
		padding: 1rem;
	}

	.footer {
		grid-area: footer;
		padding: 2rem;
		text-align: center;
	}

	/* Tablet View (min-width: 600px) */
	@media (min-width: 600px) {
		.app-shell {
			/* On tablet, we might want a max-width container or slightly different spacing */
			gap: 1.5rem;
		}

		.main {
			padding: 2rem;
		}
	}

	/* Desktop View (min-width: 1024px) */
	@media (min-width: 1024px) {
		.app-shell {
			/* Desktop: 3-column layout with content centered */
			/* 1fr (spacer) - 3fr (content) - 1fr (spacer) */
			grid-template-columns: 1fr minmax(auto, 1024px) 1fr;
			grid-template-areas:
				"header header header"
				". main ."
				"footer footer footer";
		}
		.header-content {
			padding: 0rem 1.5rem;
		}
	}
</style>
