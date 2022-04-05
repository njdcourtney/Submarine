<script>
	let content = "Starter";
</script>

<h1 class="display-1 text-center">Am I a Submarine?</h1>

<div class="container">
		{#if content == "Starter"}
				<h2 class="display-5 fw-bold text-center">Welcome</h2>
				<p class="text-center fs-4">To avoid uncertainty and doubt, this tool checks whether you're actually a submarine, despite what certain so-called 'experts' might think.</p>
				<div class="d-grid gap-2 col-6 mx-auto">
    				<button class="btn btn-primary btn-lg" type="button" on:click={() => content = "Question"}>Get started</button>
				</div>
		{:else if content == "Question"}
				<h2 class="display-5 fw-bold text-center">Question 1</h2>
				<p class="text-center fs-4">Is your name Nora?</p>
				<div class="d-grid gap-2 col-6 mx-auto">
					<button class="btn btn-success btn-lg" type="button" on:click={() => content = "Yes"}>Yes</button>
					<button class="btn btn-primary btn-lg" type="button" on:click={() => content = "No"}>No</button>
				</div>
		{:else if content == "Yes"}
				<h2 class="display-5 fw-bold text-center">Yes you are a Submarine!</h2>
				<img class="img-fluid mx-auto d-block" src="/favicon.png" alt="Yellow Submarine">
				<p class="text-center fs-4">Our panel has decided that yes, you're definitely a submarine.</p>
				<div class="d-grid gap-2 col-6 mx-auto">
					<button class="btn btn-link btn-lg" type="button" on:click={() => content = "Starter"}>Home</button>
				</div>
		{:else if content == "No"}
				<h2 class="display-5 fw-bold text-center">Sorry</h2>
				<p class="text-center fs-4">You do not appear to be a submarine.</p>
				<div class="d-grid gap-2 col-6 mx-auto">
					<button class="btn btn-link btn-lg" type="button" on:click={() => content = "Starter"}>Home</button>
				</div>
		{:else}
				<p>Ooopse, something went wrong {content}</p>
		{/if}
</div>



