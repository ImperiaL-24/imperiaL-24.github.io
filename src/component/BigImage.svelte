
<script lang="ts">
import { getContext } from "svelte";
const { setView } = getContext("view");

export let img: string | null;
export let meta: string | null;

let update = () => {
    setView(false);
}
    
</script>

<div class="bg" on:click={update}>
    <div class="image">
        <img src={img} alt="zoomed in"/>
        <p class="meta">{meta}</p>
    </div>
</div>


<style lang="scss">
	.bg {
        position: fixed;
        width: 100%;
        height: 100%;
        top: 0;
        background-color: rgba(32, 24, 41, 0.514);

        display: flex;
        justify-content: center;

        .image {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            max-width: 100%;

            img {
                width: 90vmin;
                image-rendering: pixelated;
            }

            .meta {
                font-size: 50px;
                margin: 10px;
            }
        }
    }
</style>