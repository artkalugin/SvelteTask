<script>
    export let title;
    export let author;
    export let date;
    export let content;
</script>

<h2>{title || 'Untitled post'}</h2>
<b>{author || 'Unknown author'}</b>
<em>{date || new Date().toDateString()}</em>
<p>{content || 'This post has no content'}</p>
