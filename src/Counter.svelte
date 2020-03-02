<script>
	import Button from './Button.svelte'

	let count = 0
	let emoji = '😎'

	const aumentar = () => {
		count++
		count >= 5 ? emoji = '😵' : emoji = '😁'
	}

	const disminuir = () => {
		count--
		if(count <= 0){
			count = 0
			emoji = '🤦‍♀️'
		} else {
			emoji = '🤪'
		}
	}

	const resetear = () => {
		count = 0
		emoji = '🤦‍♀️'
	}

</script>

<main>
	<h1>Hello Svelte {emoji}</h1>

	<p>{count} {count == 0 ? emoji = '👽' : ''}</p>
	
	<Button 
		name = 'Aumentar'
		handleClick = {aumentar}
	/>

	<Button 
		name = 'Disminuir'
		handleClick = {disminuir}
	/>

	<Button 
		name = 'Resetear'
		handleClick = {resetear}
	/>

</main>

<style>

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		width: 50%
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 3em;
		font-weight: 100;
	}

	p {
		font-size: 27px;
  	font-weight: bolder;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>