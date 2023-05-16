<script lang="ts">
  export let date: string | undefined = undefined;
  export let title: string | undefined = undefined;
  export let dotClass: string = '';
</script>

<div class='py-1'>
  <div class={`rounded-full h-5 w-5 -ms-7 absolute ${dotClass}`} />
  <div class="text-black">
    {#if date !== undefined}
      {date}
    {/if}
  </div>
  {#if title !== undefined}
    <div class="font-bold pb-4">{title}</div>
  {/if}
</div>
