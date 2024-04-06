<script>
    import Header from "./Header.svelte";
    import './styles.css';
</script>

<div class="app">
    <Header />

    <main>
        <!-- Content non mobile devices -->
        <slot />
        <!-- Content mobile devices -->
        <slot name="mobile" />
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