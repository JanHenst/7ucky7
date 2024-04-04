<script>
    import mainLogo from '$lib/images/mainLogo.svg';
    import starLine from '$lib/images/starLine.svg';
    import RepeatingText from "./RepeatingText.svelte";
</script>

<svelte:head>
    <title>Home</title>
    <meta name="description" content="7ucky7 website" />
</svelte:head>

<div class="main-container">
    <img src={mainLogo} alt="Main logo" />

    <div class="repeating-text-container">
        <RepeatingText />
        <RepeatingText />
        <RepeatingText />
    </div>

    <img src={starLine} alt="Main logo" />
</div>

<style>
    img {
        width: 100%;
    }

    .repeating-text-container {
        display: flex;
        justify-content: space-between;
        margin: 1rem 0 clamp(1rem, 5vw, 4rem);
    }
</style>