<script lang="ts">
	const tags: {
		name: string;
	}[] = [
		{
			name: 'All'
		},
		{
			name: 'Gaming'
		},
		{
			name: 'Music'
		},
		{
			name: 'Mixes'
		},
		{
			name: 'Posts'
		},
		{
			name: 'Rocket League'
		},
		{
			name: 'Computer Programming'
		},
		{
			name: 'Podcasts'
		},
		{
			name: 'Computers'
		},
		{
			name: 'Motivation'
		},
		{
			name: 'Weight Training'
		},
		{
			name: 'Memes'
		},
		{
			name: 'Gadgets'
		},
		{
			name: 'Action-adventure games'
		},
		{
			name: 'Comedy'
		}
	];
</script>

<div class="tags">
	{#each tags as { name }}
		<div>
			<h1>{name}</h1>
		</div>
	{/each}
</div>

<style>
	.tags {
		display: flex;
		max-width: 100%;
		flex-wrap: wrap;
		overflow-y: auto scroll;
		margin-bottom: 0;
	}

	.tags div {
		margin: 5px;
		border-radius: 5px;
		padding: 5px;
		background: rgba(0, 0, 0, 7%);
		cursor: pointer;
		transition: 0.5s;
	}

	.tags div:hover {
		background: rgba(0, 0, 0, 12%);
	}

	.tags div h1 {
		padding: 5px;
		padding-top: 0;
		padding-bottom: 0;
		font-size: 1rem;
	}
</style>
