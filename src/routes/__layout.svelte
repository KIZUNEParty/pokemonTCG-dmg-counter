<script lang="ts">
	import '../app.css';
</script>

<main>
	<slot />
</main>

<footer>
	<span>
		if u want to donate <a href="https://detzz.in.th/Donation">Click Me</a>
	</span>
	<br><br>
	<span>
		&copy; 2022 <a href="https://suphakit.net">Suphakit P.</a> All Right Reserved.
	</span>
</footer>

<style>
	main {
		width: 100%;
		height: 100vh;
	}

	footer {
		width: 100%;
		position: fixed;
		bottom: 0;

		background-color: whitesmoke;
		color: #2e2f2f;

		padding: 1rem;
		padding-left: 0;
		padding-right: 0;

		text-align: center;
		margin-left: auto;
		margin-right: auto;
	}

	footer a {
		color: #2e2f2f;
		text-decoration: underline;
	}

	footer a:hover {
		color: #2e2f2f;
		text-decoration: none;
	}
</style>
