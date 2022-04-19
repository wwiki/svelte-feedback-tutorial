<script>
	let firstName='Shawna';
	let lastName="Yuan";
	let color = 'lightgreen'
	let showText = false

	$: name = firstName + ' ' + lastName

	const toggle = ()=> {
		color = color === 'lightgreen' ? 'red' : 'lightgreen'
		showText = !showText
	}
	// 20:24
	//  npm run dev
	// prettier?
</script>

<main class="container">
	<h1 style="color: {color}">Hello {name}!</h1>

	{#if showText}
		<p>yohohoho</p>
	{:else}
		<p>no text</p>
	{/if}

	<button on:click={toggle}>Click</button>
</main>
