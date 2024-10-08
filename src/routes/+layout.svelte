<script>
	import { page } from '$app/stores';
</script>

<div>
	<nav>		
		<a href="#dialog-main">Open dialog</a>
        <a href="/">Close dialog</a>
	</nav>
	<main>
		{#if $page.url.hash === '#dialog-main'}
			<div class="dialog" id="dialog-main">
				<h2>Hello from dialog</h2>
				<a href={$page.url.pathname}>Close dialog</a>
			</div>
		{/if}
	</main>
	<footer>
			<pre>Hash is: {$page.url.hash}</pre>
	</footer>
</div>

<style>
.dialog {
	border: 2px solid rebeccapurple;
}
</style>