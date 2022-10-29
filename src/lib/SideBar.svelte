<div class="sidebar">
	<div>
		<svg
			viewBox="0 0 24 24"
			preserveAspectRatio="xMidYMid meet"
			focusable="false"
			class="style-scope yt-icon"
			style="pointer-events: none; display: block;"
			><g class="style-scope yt-icon"
				><path d="M4,10V21h6V15h4v6h6V10L12,3Z" class="style-scope yt-icon" /></g
			></svg
		>
		<h1>Home</h1>
	</div>

	<div>
		<svg
			viewBox="0 0 24 24"
			preserveAspectRatio="xMidYMid meet"
			focusable="false"
			class="style-scope yt-icon"
			style="pointer-events: none; display: block;"
			><g height="24" viewBox="0 0 24 24" width="24" class="style-scope yt-icon"
				><path
					d="M10 14.65v-5.3L15 12l-5 2.65zm7.77-4.33c-.77-.32-1.2-.5-1.2-.5L18 9.06c1.84-.96 2.53-3.23 1.56-5.06s-3.24-2.53-5.07-1.56L6 6.94c-1.29.68-2.07 2.04-2 3.49.07 1.42.93 2.67 2.22 3.25.03.01 1.2.5 1.2.5L6 14.93c-1.83.97-2.53 3.24-1.56 5.07.97 1.83 3.24 2.53 5.07 1.56l8.5-4.5c1.29-.68 2.06-2.04 1.99-3.49-.07-1.42-.94-2.68-2.23-3.25zm-.23 5.86l-8.5 4.5c-1.34.71-3.01.2-3.72-1.14-.71-1.34-.2-3.01 1.14-3.72l2.04-1.08v-1.21l-.69-.28-1.11-.46c-.99-.41-1.65-1.35-1.7-2.41-.05-1.06.52-2.06 1.46-2.56l8.5-4.5c1.34-.71 3.01-.2 3.72 1.14.71 1.34.2 3.01-1.14 3.72L15.5 9.26v1.21l1.8.74c.99.41 1.65 1.35 1.7 2.41.05 1.06-.52 2.06-1.46 2.56z"
					class="style-scope yt-icon"
				/></g
			></svg
		>

		<h1>Shorts</h1>
	</div>

	<div>
		<svg
			viewBox="0 0 24 24"
			preserveAspectRatio="xMidYMid meet"
			focusable="false"
			class="style-scope yt-icon"
			style="pointer-events: none; display: block;"
			><g class="style-scope yt-icon"
				><path
					d="M10,18v-6l5,3L10,18z M17,3H7v1h10V3z M20,6H4v1h16V6z M22,9H2v12h20V9z M3,10h18v10H3V10z"
					class="style-scope yt-icon"
				/></g
			></svg
		>

		<h1>Subscriptions</h1>
	</div>

	<div>
		<svg
			viewBox="0 0 24 24"
			preserveAspectRatio="xMidYMid meet"
			focusable="false"
			class="style-scope yt-icon"
			style="pointer-events: none; display: block;"
			><g class="style-scope yt-icon"
				><path
					d="M11,7l6,3.5L11,14V7L11,7z M18,20H4V6H3v15h15V20z M21,18H6V3h15V18z M7,17h13V4H7V17z"
					class="style-scope yt-icon"
				/></g
			></svg
		>

		<h1>Library</h1>
	</div>
</div>

<style>
	.sidebar {
		display: flex;
		flex-direction: column;
		justify-content: center;
		position: fixed;
		top: 0;
		bottom: 0;
		height: max-content;
		margin: auto;
		border-top-right-radius: 20px;
		border-bottom-right-radius: 0px;
		backdrop-filter: blur(5px);
		box-shadow: 0 0 3px rgb(0, 0, 0, 15%);
		z-index: 1;
	}

	.sidebar svg {
		width: 24px;
		height: 24px;
		cursor: pointer;
		padding: 5px;
	}

	.sidebar div {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 5px;
		padding-bottom: 15px;
		cursor: pointer;
		transition: 0.3s;
	}

	.sidebar div:hover {
		border-top-right-radius: 25px;
		background: rgba(0, 0, 0, 10%);
	}

	.sidebar div h1 {
		font-size: 0.65rem;
		margin: 0;
		padding: 0;
	}

	@media screen and (max-width: 750px) {
		.sidebar {
			bottom: initial;
			left: 0;
			right: 0;
			flex-direction: row;
		}

		.sidebar div:hover {
			border-top-right-radius: initial;
			background: initial;
			cursor: default;
		}
	}
</style>
