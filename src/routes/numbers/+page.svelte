<script>
	let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18];
	let visible = 'all';

	function new_number_array() {
		let number_array = [];
		for (let i = 0; i < 20; i++) {
			number_array.push(Math.ceil(Math.random() * 100));
		}
		return number_array;
	}
</script>

<section>
	<h1>numbers!</h1>
    <button on:click="{() => numbers = new_number_array()}">new numbers</button>

    <br>
	<label>
		<input type="radio" bind:group={visible} name="visible" value="all" />
		all
	</label>
	<label>
		<input type="radio" bind:group={visible} name="visible" value="odd" />
		odd
	</label>
	<label>
		<input type="radio" bind:group={visible} name="visible" value="even" />
		even
	</label>
	<table>
		{#each numbers as number}
			{#if visible == 'all'}
				<row>{number}</row><br />
			{:else if visible == 'odd' && number % 2 != 0}
				<row>{number}</row><br />
			{:else if visible == 'even' && number % 2 == 0}
				<row>{number}</row><br />
			{/if}
		{/each}
	</table>
</section>
