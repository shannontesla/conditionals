<script lang="ts">
	import Message from "./components/Message.svelte";

	let show = true;
	const handleToggle = () => {
		show = !show;
	}
</script>

<main>

	{#if show}
		<Message />
	{:else}
		console.log("")
	{/if}
	<button on:click={handleToggle}>Hidden/Shown</button>
</main>

<style>
	main {
		text-align: center;
		background-color: azure;
		color: black;
	}
	button {
		background-color: blueviolet;
		border-radius: 1.5em;
		color: white;
		border: none;
		padding: 10px;
		margin: 10px;
	}
</style>