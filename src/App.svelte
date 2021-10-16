<script>
	
	let Color ='Adama';
	let firstName = 'Adama';
	let lastName = 'Diallo';

	$: fullName = firstName+ ' ' +lastName ;
	
	const handleClick = () => 
	{	
		Color = 'Black'
	};

	const handleInput = (e) => {
		fullName = e.target.value;

	};
</script>

<main>
	
	<h1> {fullName} - {Color} ! </h1>
	<!-- <button on:click={handleClick}>Change le nom</button> -->
	<!-- <input type="text" on:input={handleInput} value = {nom}> -->
	
	<input type="text" bind:value={firstName}>
	<input type="text" bind:value={lastName}>
	<input type="text" bind:value={Color}>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>