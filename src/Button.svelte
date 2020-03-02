<script>
  export let name = ''
	export let handleClick
</script>

<button on:click={handleClick}> {name} </button>

<style>
  button {
		width: 100%;
		height: 2rem;
    padding: 0.2em;
		background-color: beige;
		border-radius: 1em;
    cursor: pointer;
		color: #000
	}

	button:hover {
		width: 100%;
		height: 2rem;
    padding: 0.2em;
		background-color: #ccc;
		border-radius: 1em;
    cursor: pointer;
		color: #fff
	}

	@media (min-width: 640px) {
			button {
			width: 100%;
			height: 2rem;
			padding: 0.2em;
			background-color: beige;
			border-radius: 1em;
			cursor: pointer;
			color: #000
		}

		button:hover {
			width: 100%;
			height: 2rem;
			padding: 0.2em;
			background-color: #ccc;
			border-radius: 1em;
			cursor: pointer;
			color: #fff
		}
	}
</style>