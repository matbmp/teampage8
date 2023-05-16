<script>
    import Header from "./Header.svelte";
</script>

<div>
    <Header/>
    <slot/>
</div>

<style>
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

    :global(body){
        margin: 0;
    }
</style>