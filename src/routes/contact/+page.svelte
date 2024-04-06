<svelte:head>
    <title>Contact</title>
    <meta name="description" content="7ucky7 contact page" />
</svelte:head>

<div class="contact-container">
    <h1>contact.</h1>
    <div>
        <p>my brand instagram page:</p>
        <a href="https://www.instagram.com/7ucky7.nl?igsh=MWZkZmFlZzJ5NTYxbQ==" target="_blank">@7ucky7.nl</a>
    </div>
    <div>
        <p>my personal instagram page:</p>
        <a href="https://www.instagram.com/josefienvdhenst?igsh=MWdjbnB3ejcydXdzMw==" target="_blank">@josefienvdhenst</a>
    </div>
    <div>
        <p>my business email:</p>
        <p>madebylucky7@gmail.com</p>
    </div>
</div>

<style>
    .contact-container {
        display: flex;
        flex-direction: column;
        align-items: baseline;
    }

    .contact-container div {
        margin-bottom: 1rem;
    }

    h1 {
        margin-bottom: 0.5rem;
        font-size: clamp(1.5rem, 10vw, 5rem);
    }

    p, a {
        margin: 0;
        font-size: clamp(1rem, 1.5vw, 2rem);
    }
</style>