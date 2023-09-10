<script>
	import { page } from '$app/stores';
    import './styles.css'
</script>

<header>
	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/fruits' ? 'page' : undefined}>
				<a href="/fruits">Fruit</a>
			</li>
            <li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>
			<li aria-current={$page.url.pathname === '/numbers' ? 'page' : undefined}>
				<a href="/numbers">Numbers</a>
			</li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: center;
        background-color: gray;
        border-radius: 1em;
	}

	nav {
		display: flex;
		justify-content: space-around;
		--background: rgba(255, 255, 255, 0.7);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page'] {
		border: solid rgba(0,0,0,255);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		background-color: rgba(200,200,200,100);
	}
</style>
