<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	let gxClass :any = ''
	let vsClass :any = ''

	let active :number = 0;
	let fst :number = 0;
	let snd :number = 0;
	let trd :number = 0;
	let fth :number = 0;
	let ffth :number = 0;
	let sth :number = 0;
	let svth :number = 0;

	// let dClass :any = '0'
	// let dice :any;

	let coin :any = -1;
	let cCheck :number = 0

	if (cCheck == 1) {
		coin = Math.floor(Math.random() * 2) + 1;
		cCheck = 0;
	}

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
				<button class={'GX ' + gxClass} style="width: 13rem;" on:click={e => gxClass = 'activated'}>
					<h1>
						GX
					</h1>
				</button>
				<br><br><br>
				<button class={'v-star ' + vsClass} style="width: 13rem;" on:click={e => vsClass = 'activated'}>
					<h1>
						V-Star
					</h1>
				</button>
			</div>
			<div class="card">
				<div class="dmg-container">
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
				</div>

				<br><br>

				<button class="setzero" on:click={e=> active = 0}>
					Set to '0'
				</button>
			</div>
			<div class="control">
				<!-- <button class="random" on:click={e => dClass = ''}>
					{#if dClass == ''}
						<span>
							{dice = Math.random() * 6}
						</span>
					{:else}
						<i class="fa-solid fa-dice"></i>
					{/if}
				</button> -->

				<!-- <br><br><br> -->

				<button class="random" on:click={e => coin = Math.floor(Math.random() * 2) + 1}>
					{#if coin == 1}
						H
					{:else if coin == 2}
						T
					{:else}
						C
					{/if}
				</button>
			</div>
		</div>

		<div class="bench-pokemon">
			<div class="card">
				<div class="dmg-container">
					<button on:click={e => fst = fst - 10}>
						-
					</button>
					&nbsp;&nbsp;
					<span class="dmg fst">
						{fst}
					</span>
					&nbsp;&nbsp;
					<button on:click={e => fst = fst + 10}>
						+
					</button>
				</div>

				<br><br>

				<button class="setzero" on:click={e=> fst = 0}>
					Set to '0'
				</button>
			</div>

			<div class="card">
				<div class="dmg-container">
					<button on:click={e => snd = snd - 10}>
						-
					</button>
					&nbsp;&nbsp;
					<span class="dmg snd">
						{snd}
					</span>
					&nbsp;&nbsp;
					<button on:click={e => snd = snd + 10}>
						+
					</button>
				</div>

				<br><br>

				<button class="setzero" on:click={e=> snd = 0}>
					Set to '0'
				</button>
			</div>

			<div class="card">
				<div class="dmg-container">
					<button on:click={e => trd = trd - 10}>
						-
					</button>
					&nbsp;&nbsp;
					<span class="dmg trd">
						{trd}
					</span>
					&nbsp;&nbsp;
					<button on:click={e => trd = trd + 10}>
						+
					</button>
				</div>

				<br><br>

				<button class="setzero" on:click={e=> trd = 0}>
					Set to '0'
				</button>
			</div>

			<div class="card">
				<div class="dmg-container">
					<button on:click={e => fth = fth - 10}>
						-
					</button>
					&nbsp;&nbsp;
					<span class="dmg fth">
						{fth}
					</span>
					&nbsp;&nbsp;
					<button on:click={e => fth = fth + 10}>
						+
					</button>
				</div>

				<br><br>

				<button class="setzero" on:click={e=> fth = 0}>
					Set to '0'
				</button>
			</div>

			<div class="card">
				<div class="dmg-container">
					<button on:click={e => ffth = ffth - 10}>
						-
					</button>
					&nbsp;&nbsp;
					<span class="dmg ffth">
						{ffth}
					</span>
					&nbsp;&nbsp;
					<button on:click={e => ffth = ffth + 10}>
						+
					</button>
				</div>

				<br><br>

				<button class="setzero" on:click={e=> ffth = 0}>
					Set to '0'
				</button>
			</div>
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

	.GX, .v-star {
		background-color: coral;
		color: whitesmoke;

		border: none;
		border-radius: 10px;
	}

	.activated {
		opacity: 0.2;
	}

	.control .random {
		width: 75px;
		height: 75px;

		background-color: coral;
		color: whitesmoke;

		text-align: center;
		align-items: center;

		font-size: 40px;

		border: none;
		border-radius: 50%;
	}

	.control .random:hover {
		opacity: 0.8;
		cursor: pointer;
	}

	.active-pokemon {
		width: 100%;
		height: 50vh;

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

	.bench-pokemon {
		width: 100%;
		height: 50vh;

		display: flex;
		flex-direction: row;

		text-align: center;
		vertical-align: middle;
	}

	.card {
		width: 60%;
		height: 30vh;

		display: flex;
		flex-direction: column;
		text-align: center;
		vertical-align: middle;
		align-items: center;
		align-content: center;

		background-color: grey;
		padding: 1rem;
		border-radius: 10px;
		margin: 1rem;

		vertical-align: middle;
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
