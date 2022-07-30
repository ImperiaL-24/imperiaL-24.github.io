<script lang="ts">

export let URL: string | null = null;
export let text: string | null = null;
export let img: string;
const redirect = () => {
    if(URL == null) return;
    window.location.href = URL;
}

</script>

<div on:click={redirect}>

    <img src={img} alt={text}/>
    <p>{text}</p>
</div>


<style lang="scss">

    div {
        padding: 1em;
        width: 400px;
        background-color: white;
        border-radius: 15px;
        margin: 10px 20px;
        display: flex;
        align-items:  center;
        transition: all 0.5s;
        

        img {
            width: 72px;
            height: 72px;
            border-radius: 15px;
        }

        p {
            margin: auto;
        }

        &:hover {
            background: rgb(175, 177, 179);
        }
    }

</style>