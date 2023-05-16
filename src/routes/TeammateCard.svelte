<script>
    import Account from "virtual:icons/mdi/account";
    export let name=''
    export let role=''
</script>

<div class="flex flex-col items-center bg-slate-200 p-4 rounded-lg">
    <Account class='text-9xl'/>
    <div class="text-xl font-bold pt-4">{name}</div>
    <div class="text-lg">{role}</div>
</div>