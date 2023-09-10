<script>
	let fruits = [
		'avocado',
		'eggplant',
		'cucumber',
		'pear',
		'peach',
		'kiwi',
		'apple',
		'mango',
		'grape',
		'orange',
		'cherry',
		'watermelon',
		'lychee',
		'apricot',
		'banana',
		'blueberry',
		'date',
		'coconut',
		'plum',
		'pineapple',
		'raspberry',
		'star fruit',
		'lemon',
		'lime',
		'blackberry',
		'honeydew',
		'tangerine',
		'pomegranate'
	].sort();
	let visible = [ false, false];
</script>

<section>
	<h1>fruits!</h1>
	<br />
	<b>include those that have:</b>
	<br />
	<label>
		<input type="checkbox" name="visible" bind:checked={visible[0]} />
		the letter a
	</label>
	<label>
		<input type="checkbox" name="visible" bind:checked={visible[1]} />
		More than 5 letters
	</label>
	<br />
	<br />
	<table>
		{#each fruits as fruit}
			{#if visible[0] && fruit.toLowerCase().includes('a')}
				<row>{fruit}</row><br />
			{:else if visible[1] && fruit.length > 5}
				<row>{fruit}</row><br />
			{/if}
		{/each}
	</table>
</section>

<style>
    section{
        margin-bottom: 4.5em;
    }
</style>
