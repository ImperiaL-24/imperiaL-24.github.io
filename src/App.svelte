<script lang="ts">
import Intro from "./Intro.svelte";
import Database from "./Database.svelte";
import Image from "./component/Image.svelte";
import Content from "./component/Content.svelte";
import ListElem from "./component/ListElem.svelte";
import { setContext } from "svelte";
import BigImage from "./component/BigImage.svelte";

let isViewingBig: boolean = false;
let image: string | null;
let meta: string | null;

setContext("view", {
	setView: (newView: boolean) => isViewingBig = newView,
	setImage: (newImg: string, newMeta: string) =>  {
		image = newImg
		meta = newMeta
	}
});

$: document.body.classList.toggle('scroll-lock', isViewingBig);

</script>

<main>
	<Intro></Intro>
	<Database title="PORTOFOLIO">
		<Database title="Items">
			<Image img="portofolio/weapon.png" meta="Swords and weapons. Created: End of 2021"></Image>
			<Image img="portofolio/arrows.png" meta="Arrow types. Created: End of 2021"></Image>
			<Image img="portofolio/armor_icons.png" meta="Armor icons. Created: Middle of 2021"></Image>
			<Image img="portofolio/misc.png" meta="Misc items. Created: Middle of 2021"></Image>
			<!--<Image img="portofolio/gems.png" meta="Gem designs. Created: Middle of 2022"></Image>-->
		</Database>
		<Database title="GUI">
			<Image img="portofolio/gui.png" meta="Prototype book gui. Created: Middle of 2022"></Image>
			<Image img="portofolio/gui2.png" meta="Prototype steapunk gui. Created: Middle of 2022"></Image>
		</Database>
		<Database title="Font Textures">
			<Image img="portofolio/icons.png" meta="Player icons. Created: Middle of 2022"></Image>
		</Database>
		<Database title="3D Models">
			<Image img="portofolio/model.png" meta="Gun with a default style. Created: Middle of 2022"></Image>
			<Image img="portofolio/model2.png" meta="Backpack with a default style. Created: Middle of 2022"></Image>
		</Database>
		
	</Database>
	<Database title="PROJECTS" theme="dark">        
		<Content img="phq.webp" title="PacksHQ" description="Hypixel Skyblock Pack" button="https://packshq.com/"></Content>
        <Content img="res.png" title="Returned Studios" description="Minecraft Products" button="https://discord.gg/Y4AJg49GuQ"></Content>
	</Database>
	<Database title="CONTACT">        
		<ListElem text="Discord - T-34-85#4572" URL="https://discord.gg/Y4AJg49GuQ" img="discord.png"></ListElem>
        <ListElem text="MCMarket - ImperiaL24" URL="https://www.mc-market.org/members/386162/" img="mcm.png"></ListElem>
	</Database>
</main>
{#if isViewingBig}
	<BigImage img={image} meta={meta}></BigImage>
{/if}
	
<style lang="scss">

	main {
		text-align: center;
		margin: 0 auto;
		overflow: auto;
		position: absolute;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>