<script>
    import { onMount } from 'svelte';
    import Header from "./Header.svelte";
    import './styles.css';
    import MobileContent from "./MobileContent.svelte";

    let isMobile = false;

    onMount(() => {
        const checkMobile = () => {
            isMobile = window.matchMedia('(max-width: 600px)').matches;
        };

        checkMobile();
        window.addEventListener('resize', checkMobile);

        return () => {
            window.removeEventListener('resize', checkMobile);
        };
    });
</script>

<div class="app">
    <Header isMobile="{isMobile}" />

    <main>
        {#if !isMobile}
            <slot />
        {:else}
            <MobileContent />
        {/if}
    </main>
</div>

<style>
    .app {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    main {
        flex: 1;
        display: flex;
        flex-direction: column;
        padding: 1rem;
        width: 85vw;
        max-width: 100rem;
        margin: 0 auto;
        box-sizing: border-box;

        @media screen and (max-width: 426px){
            width: 95vw;
        }
    }
</style>