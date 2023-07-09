<script>
    export let href = '#';
    export let content = '';
    export let classes = 'hidden md:block p-3 px-6 text-white bg-brightRed rounded-full baseline hover:bg-brightRed';
</script>

<a href={href} class={classes}>{content}</a>