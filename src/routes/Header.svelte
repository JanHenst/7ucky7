<script>
	import { page } from '$app/stores';
	import logo from '$lib/images/headerLogo.svg';
	import headerStars from '$lib/images/headerStars.svg';
	export let isMobile = false;
</script>

<header>
	<div class="corner">
		<div class="header-logo-container">
			<a href="/">
				<img src={logo} alt="Lucky7 logo" />
			</a>
			<p>designed and made by: <br> josefien van der henst</p>
		</div>
	</div>

	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/projects' ? 'page' : undefined}>
				<a href={!isMobile ? "/projects" : "#projects"}>PROJECTS</a>
			</li>
			<li class="line">|</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href={!isMobile ? "/about" : "#about"}>ABOUT</a>
			</li>
			<li class="line">|</li>
			<li aria-current={$page.url.pathname === '/contact' ? 'page' : undefined}>
				<a href={!isMobile ? "/contact" : "#contact"}>CONTACT</a>
			</li>
		</ul>
	</nav>

	<div class="corner">
		<img src={headerStars} alt="Stars in the top right corner" />
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;

		@media (max-width: 900px) {
			align-items: center;
		}
	}

	.corner {
		width: clamp(6em, 15vw, 10rem);
		height: clamp(2em, 8vw, 6rem);
		display: flex;
		justify-content: center;
		align-items: center;

		@media (max-width: 900px) {
			height: 100%;
		}
	}

	.corner img {
		width: 100%;
		max-width: clamp(3rem, 12vw, 7rem);
		object-fit: contain;
	}

	.header-logo-container {
		text-align: center;

		@media (max-width: 900px) {
			margin-top: 6px;
		}
	}

	.header-logo-container p {
		font-size: clamp(0.25rem, 1vw, 0.5rem);
		margin: 0.25rem 0 0 0;
	}

	.header-logo-container a {
		display: flex;
	}

	nav {
		display: flex;
		justify-content: center;

		@media (min-width: 900px) {
			height: 4rem;
		}
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
	}

	li {
		font-size: clamp(0.5rem, 2.5vw, 2rem);
	}

	.line {
		margin: 0 clamp(1rem, 5vw, 2rem) 0.25rem;
	}
</style>
