<script>
    import ProjectComponent from "./ProjectComponent.svelte";
</script>

<svelte:head>
    <title>Projects</title>
    <meta name="description" content="7ucky7 projects page" />
</svelte:head>

<div class="project-container">
    <h1>projects.</h1>
    <div class="projects">
        <ProjectComponent text="upcycled items" />
        <ProjectComponent text="from scratch" />
        <ProjectComponent text="upcycled bags" />
        <ProjectComponent text="art & more" />
        <ProjectComponent text="magazine" />
        <ProjectComponent text="graphic design" />
    </div>
</div>

<style>
    .project-container {
        display: flex;
        flex-direction: column;
        align-items: baseline;
    }

    .projects {
        margin-top: clamp(1rem, 3vw, 2.5rem);
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;
        row-gap: clamp(1rem, 3vw, 2.5rem);
        column-gap: 2.5rem;

        @media screen and (max-width: 768px) {
            column-gap: 1rem;
            /*justify-content: center;*/
        }
    }

    h1 {
        margin-bottom: 0.5rem;
        font-size: clamp(1.5rem, 7vw, 5rem);
    }
</style>