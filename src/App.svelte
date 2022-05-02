<script>
  import MaskInput from "svelte-input-mask/MaskInput.svelte";
  import Button from "./Button.svelte";
  import Post from "./Post.svelte";

  let posts = [
    {
      title: "Lorem Ipsum",
      author: "Artemii Kalugin",
      date: "April 26, 2022",
      content: "Lorem ipsum dolor sit amet",
    },
    {
      title: "Ipsum Lorem",
      author: "John Smith",
      date: "April 18, 2022",
      content: "Amet sit dolor ipsum lorem",
    },
  ];

  let maskString = "DD.MM.YYYY";
  let mask = "00.00.0000";

  const createPost = (evt) => {
    const formData = new FormData(evt.target);
    const data = {};
    for (let field of formData) {
      const [key, value] = field;
      data[key] = value;
    }
    posts = [data, ...posts];
    evt.target.reset();
  };
</script>

<main>
  <h1>SvelteTask</h1>
  <form on:submit|preventDefault={createPost}>
    <input type="text" name="title" placeholder="Title" required />
    <input type="text" name="author" placeholder="Author" required />
    <MaskInput
      {maskString}
      {mask}
      name="date"
      placeholder="Date ({maskString})"
    />
    <textarea name="content" placeholder="Content" rows="5" />
    <Button variant="success">Submit</Button>
  </form>
  <div class="posts">
    {#each posts as post}
      <Post {...post} />
    {/each}
  </div>
</main>

<style>
  main {
    padding: 1em;
    max-width: 600px;
    margin: 0 auto;
  }

  form {
    display: grid;
    grid-template-columns: 1fr;
  }

  .posts {
    margin-top: 1.5em;
    display: grid;
    grid-template-columns: 1fr;
    gap: 1em;
  }
</style>
