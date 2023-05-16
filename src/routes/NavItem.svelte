<script lang='ts'>
    let klass: string = '';
    export {klass as class}
</script>

<button class='p-2 mx-2 rounded-lg hover:text-amber-600 text-black {klass}' on:click>
    <slot/>
</button>