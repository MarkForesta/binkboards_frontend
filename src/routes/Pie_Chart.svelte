<script lang="ts">
    import { ConicGradient } from '@skeletonlabs/skeleton';
    import type { ConicStop } from '@skeletonlabs/skeleton';    
    
    // TODO: Determine size of gradient by doing tournament manipulation
    const conicStops: ConicStop[] = [
	{ label: "Winner", color: '#ffbf00', start: 0, end: 10 }, // FIRST
	{ label: "Second", color: '#c0c0c0', start: 10, end: 35 }, // Second
	{ label: "Thrid", color: '#cd7f32', start: 35, end: 40 }, // Thrid
    { label: "FT HYPE", color: 'blue', start: 40, end: 50 }, // FT
    { label: "ITM", color: '#036704', start: 50, end: 80 }, // ITM
	{ label: "Need Help", color: 'red', start: 80, end: 100 } // NOTHING

];

</script>


<ConicGradient  stops={conicStops} legend width="w-1/2" regionLegend="text-lg"></ConicGradient>