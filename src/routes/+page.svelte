<script>
	import MainVideos from '$lib/MainVideos.svelte';
	import SideBar from '$lib/SideBar.svelte';
</script>

<svelte:head>
	<title>Youtube</title>
</svelte:head>

<div class="main">
	<SideBar />

	<div class="secondary">
		<MainVideos />
	</div>
</div>

<style>
	.main {
		display: flex;
		height: 100%;
	}
</style>
