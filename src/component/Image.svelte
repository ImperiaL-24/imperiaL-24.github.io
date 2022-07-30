<script lang="ts">
    import { getContext } from "svelte";
    

export let img: string | null = null;
export let meta: string; 
    const { setView, setImage } = getContext("view");
    let update = () => {
        setView(true);
        setImage(img, meta);
        console.log("ee")
    }
    
    
</script>

<div on:click={update} style="background-image: url({img});">
</div>

<style lang="scss">
	div {
        width: 400px;
        height: 300px;
        background-color: white;
        border-radius: 15px;
        margin: 20px;
        background-repeat: no-repeat;
        background-size: 100%;
        background-position: center;
        image-rendering: pixelated;
        transition: all 0.5s;
        
        &:hover {
            background-size: 110%;
        }
    }
</style>