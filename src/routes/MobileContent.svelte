<script>
    import HomePage from './+page.svelte';
    import ProjectPage from './projects/+page.svelte';
    import AboutPage from './about/+page.svelte';
    import instaLogo from '$lib/images/instaLogo.webp';
</script>

<div>
    <HomePage />
    <div id="projects">
        <ProjectPage />
    </div>
    <div id="about">
        <AboutPage />
    </div>
    <div id="contact" class="instagram-container">
        <a href="https://www.instagram.com/7ucky7.nl?igsh=MWZkZmFlZzJ5NTYxbQ==" target="_blank">
            <img src={instaLogo} alt="Instagram logo" />
            <p>business</p>
        </a>
        <a href="https://www.instagram.com/josefienvdhenst?igsh=MWdjbnB3ejcydXdzMw==" target="_blank">
            <img src={instaLogo} alt="Instagram logo" />
            <p>personal</p>
        </a>
    </div>
</div>

<style>
    .instagram-container {
        display: flex;
        justify-content: center;
        margin-top: 2rem;
    }

    .instagram-container a {
        display: flex;
        align-items: center;
    }

    .instagram-container p {
        margin: 0 0.75rem 0 0.25rem;
        font-size: 0.5rem;
    }

    img {
        max-width: 1rem;
    }
</style>