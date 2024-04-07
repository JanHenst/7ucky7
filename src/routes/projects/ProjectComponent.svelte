<script>
    import projectFolder from '$lib/images/projectFolder.svg';
    export let text = '';
</script>

<div class="project">
    <img src={projectFolder} alt="Project Folder" />
    <p>{text}</p>
</div>

<style>
    .project {
        flex-basis: calc(33.33% - 2.5rem);
        max-width: calc(33.33% - 2.5rem);

        display: flex;
        flex-direction: column;
        align-items: center;

        @media screen and (max-width: 768px) {
            flex-basis: calc(33.33% - 1rem);
            max-width: calc(33.33% - 1rem);
        }
    }

    img {
        width: clamp(5rem, 20vw, 20rem);
    }

    p {
        font-size: clamp(0.5rem, 2.25vw, 1.4rem);
    }
</style>