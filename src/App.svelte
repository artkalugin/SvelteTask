<script>
	let posts = [] // Store the posts here

	const createPost = () => {
		// Your logic to create a post goes here
	}
</script>

<main>
	<form on:submit|preventDefault={createPost}>
		<input type="text" name="title" placeholder="Title" required /><br />
		<input type="text" name="author" placeholder="Author" required /><br />
		<input type="text" name="date" placeholder="Date" /><br />
		<textarea name="content" placeholder="Content"></textarea><br />
		<button>Create</button>
	</form>
	<div class="posts">
		<!-- Your posts go here -->
	</div>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>