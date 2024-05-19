<script lang="ts">
	import { onMount } from 'svelte';
    import Tournament_binkboard from './Tournament_binkboard.svelte';
    let ms : number = 3000;
    let Newwidth : number = 250;
    let width : number = 250;
    let elemCarousel: HTMLDivElement;
    let isVisible: string = "hidden";
    let testing: HTMLDivElement;
    console.log("Width " + width)
    
    function carouselRight(): void {
    console.log(elemCarousel.scrollLeft, elemCarousel.scrollWidth, elemCarousel.clientWidth);
	const x =
		elemCarousel.scrollLeft === elemCarousel.scrollWidth - elemCarousel.clientWidth
			? 0 // loop
			: elemCarousel.scrollLeft + elemCarousel.clientWidth; // step right
	elemCarousel.scroll(x, 0);

}

onMount(() => {
        console.log("Width mount  " + width)
        Newwidth = width;
        isVisible = "visible";
        setInterval(carouselRight, ms)
    });

// TODO: The Width of the carousel should exactly be the width of one child element
</script>

<div bind:this={testing} class="card p-4 gap-4 items-center w-96" style="visibility: {isVisible}">
	<div bind:this={elemCarousel} class="snap-x snap-mandatory scroll-smooth flex overflow-x-auto">
        <div bind:clientWidth={width}>
            <Tournament_binkboard />
        </div>
        <Tournament_binkboard />
        <Tournament_binkboard />
        <Tournament_binkboard />
        <Tournament_binkboard />
        <Tournament_binkboard />
	</div>
</div>
