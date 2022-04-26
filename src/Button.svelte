<script>
    export let variant;
    export let text = 'Create';
</script>

<button class="{variant}">{text}</button>

<style>
    button {
        color: #ffffff;
        width: 150px;
        height: 40px;
        justify-self: end;
    }
</style>
