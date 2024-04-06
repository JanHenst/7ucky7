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
            flex-basis: calc(50%);
            max-width: calc(50%);
        }
    }

    img {
        width: clamp(8rem, 25vw, 20rem);
    }

    p {
        font-size: clamp(0.75rem, 2vw, 1.4rem);
    }
</style>