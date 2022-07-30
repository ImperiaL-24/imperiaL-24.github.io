<script lang="ts">
    export let img: string;
    export let title: string;
    export let description: string;
    export let button: string | null = null;
</script>


<section>
    <img src={img} alt="content"/>
    <p class="title">{title}</p>
    <p class="desc">{description}</p>
    {#if button}
    <button><a href={button}>View</a></button>
    {/if}
</section>  

<style lang="scss">

    section {
        padding: 2em;
        width: 400px;
        height: 300px;
        background: rgb(233, 238, 238);
        border-radius: 15px;
        margin: 20px;

        img {
            height: 128px;
            width: 128px;
            border-radius: 15px;
            box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
        }

        .title {
            font-weight: 400;
        }

        .desc {
            font-weight: 200;
            font-size: larger;
            padding: 10px;
        }

    }

    p {
        margin: 0;
        font-size: 2rem; 
        color: rgba(36,20,47,1);
    }


    button {
        padding: 15px;
        width: 25%;
        border-radius: 10px;
        background: none;
        border-color: rgba(36,20,47,1);
        transition: all 0.2s;

        a {
            color: rgba(36,20,47,1);
            text-decoration: none;
            transition: all 0.2s;
        }

        &:hover {
            background-color: rgba(36,20,47,1);
            
            a {
                color: white;
            }
        }

    }
</style>