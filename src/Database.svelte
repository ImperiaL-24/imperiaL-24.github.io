<script lang="ts">

export let title: String;
export let theme = "light";

</script>
<section class={theme}>
    <p class={theme}>{title}</p>
    <div class="images">
        <slot/>
    </div>

</section>

<style lang="scss">

    p {
        margin: 0;
        font-size: 2rem; 
        font-weight: 200;
    }

    .images {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }

    section {
        padding: 2em;
    }
</style>