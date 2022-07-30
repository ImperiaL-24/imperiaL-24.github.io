<section>
    <img src="pfp.png" alt="profile"/>
	<p class="title">ImperiaL</p>
    <p class="description">Pixel Artist</p>
</section>

<style lang="scss">
	section {
        display: flex;
        justify-content: end;
        align-items: center;
        flex-direction: column;
		background: linear-gradient(0deg, rgba(36,20,47,1) 0%, rgba(0,0,0,1) 100%);
        height: 500px;
	}

    img {
        box-shadow: rgba(0, 0, 0, 0.07) 0px 1px 2px, rgba(0, 0, 0, 0.07) 0px 2px 4px, rgba(0, 0, 0, 0.07) 0px 4px 8px, rgba(0, 0, 0, 0.07) 0px 8px 16px, rgba(0, 0, 0, 0.07) 0px 16px 32px, rgba(0, 0, 0, 0.07) 0px 32px 64px;
        width: 10rem;
        border-radius: 10%;
    }

    .title {
        font-size: 2.5rem;
        margin: 10px;
    }

    .description {
        margin: 60px;
        font-size: 1.25rem;
    }
</style>