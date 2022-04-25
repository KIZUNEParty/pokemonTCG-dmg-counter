<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	let active :number = 0;
	let fst :number = 0;
	let snd :number = 0;
	let trd :number = 0;
	let fth :number = 0;
	let ffth :number = 0;
	let sth :number = 0;
	let svth :number = 0;

	if (active < 0) {
		active = 0
	}
</script>

<svelte:head>
	<title>PokémonTCG Damage Counter</title>
	<meta name="description" content="Just a Counter for a lazy man who play PokémonTCG" />
</svelte:head>

<section>
	<div class="dmg-control">
		<div class="active-pokemon">
			<div class="gx-vstar">
				&nbsp;
			</div>
			<div class="card">
				<button on:click={e => active = active - 10}>
					-
				</button>
				&nbsp;&nbsp;
				<span class="dmg active">
					{active}
				</span>
				&nbsp;&nbsp;
				<button on:click={e => active = active + 10}>
					+
				</button>

				<br><br>

				<button class="setzero" on:click={e=> active = 0}>
					Set to '0'
				</button>
			</div>
			<div class="control">
				&nbsp;
			</div>
		</div>
		<div class="bench-pokemon">

		</div>
	</div>
	
	<div class="warning">
		<h1>
			please set your screen to landscape
		</h1>
	</div>
</section>

<style>
	section {
		display: block;
		width: 100%;
		height: 100vh;
	}

	.dmg-control {
		width: 100%;
		height: 100vh;
	}

	.active-pokemon {
		width: 100%;

		display: flex;
		flex-direction: row;

		text-align: center;
		vertical-align: middle;
		align-items: center;
		align-content: center;
	}

	.active-pokemon .gx-vstar {
		width: 100%;
		height: auto;
	}

	.active-pokemon .control {
		width: 100%;
		height: auto;
	}

	.card {
		width: 60%;
		background-color: grey;
		padding: 1rem;
		border-radius: 10px;
		margin: 1rem;
	}

	.card button {
		width: 40px;
		height: 40px;

		font-size: 18px;
		background-color: coral;
		color: whitesmoke;

		border: none;
		border-radius: 50%;
	}

	.card button:hover{
		opacity: 0.8;
		cursor: pointer;
	}

	.card .setzero {
		width: 80%;
		border-radius: 10px;
	}

	.warning {
		width: 100%;
		height: 100vh;

		display: none;

		text-align: center;
		vertical-align: middle;
		align-items: center;
		align-content: center;
	}

	.warning h1 {
		width: 100%;
		height: auto;

		padding: 1rem;

		text-align: center;
	}

	@media only screen and (max-width: 900px) {
		.warning {
			display: flex;
		}

		.dmg-control {
			display: none;
		}
	}
</style>
