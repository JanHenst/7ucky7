<script>
import mainLogo from "$lib/images/mainLogo.svg";
import mainLogoPng from "$lib/images/mainLogoPng.png";
import mainLogo2 from "$lib/images/mainLogo2.svg";
import mainLogo3 from "$lib/images/mainLogo3.svg";
import mainLogo4 from "$lib/images/mainLogo4.svg";
import mainLogo5 from "$lib/images/mainLogo5.svg";
import mainLogoOnlyBubble from "$lib/images/mainLogoOnlyBubble.svg";
import mainLogoOnlyScribble from "$lib/images/mainLogoOnlyScribble.svg";
</script>

<div>
<!--    <img src={mainLogo} alt="Main logo" />-->
<!--    <img src={mainLogoPng} alt="Main logo" />-->
<!--    <img src={mainLogo2} alt="Main logo" />-->
<!--    <img src={mainLogo3} alt="Main logo" />-->
    <img src={mainLogoOnlyBubble} alt="Main logo" />
    <img src={mainLogo4} alt="Main logo" />
    <img src={mainLogo5} alt="Main logo" />
    <div class="combinedLogo">
        <img src={mainLogoOnlyBubble} alt="Main logo" />
        <img src={mainLogoOnlyScribble} alt="Main logo" />
    </div>
</div>

<style>
    img {
        width: 100%;
    }

    .combinedLogo {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        margin-top: clamp(5rem, 15vw, 25rem);
    }

    .combinedLogo img {
        position: absolute;
        width: 60vw;
    }

    .combinedLogo img:nth-child(1) {
        width: 50vw;
    }
</style>