<script>
    import { ABOUT_TEXT } from '$lib/text/textConstants';
</script>

<svelte:head>
    <title>About</title>
    <meta name="description" content="7ucky7 about page" />
</svelte:head>

<div class="about-container">
    <h1>{ABOUT_TEXT.title}</h1>
    <p>
        {@html ABOUT_TEXT.paragraph1}
    </p>
    <p>
        {@html ABOUT_TEXT.paragraph2}
    </p>
    <p>
        {@html ABOUT_TEXT.paragraph3}
    </p>
</div>

<style>
    .about-container {
        display: flex;
        flex-direction: column;
        align-items: baseline;
    }

    h1 {
        margin-bottom: 0.5rem;
        font-size: clamp(1.5rem, 10vw, 5rem);
    }

    p {
        margin: 0 0 1rem;
        font-size: clamp(0.5rem, 1.35vw, 1.4rem);
    }
</style>