<script>
    export let title;
    export let author;
    export let date;
    export let content;
</script>

<div class="post">
    <h2>{title || 'Untitled post'}</h2>
    <b>{author || 'Unknown author'}</b>
    <em>{date || new Date().toDateString()}</em>
    <p>{content || 'This post has no content'}</p>
</div>


<style>
    .post {
        border: 1px solid #ddd;
        border-radius: 3px;
        padding: 1em;
        background-color: #fff;
    }

    h2 {
        margin-top: 0;
    }

    b, em {
        opacity: 0.3;
        font-weight: 300;
    }

    p {
        margin-bottom: 0;
    }
</style>