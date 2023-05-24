<script>
    import NavItem from "./NavItem.svelte";
    import {Drawer, Button} from 'flowbite-svelte'

    let navigationHidden = true;
</script>

<div class="h-screen min-h-fit flex flex-col">
    <Drawer bind:hidden={navigationHidden}>
        <nav class="flex flex-col">
            <NavItem>Zespół</NavItem>
            <NavItem>Harmonogram</NavItem>
            <NavItem>Przebieg</NavItem>
            <NavItem>Raporty</NavItem>
            <NavItem>Dokumentacja</NavItem>
        </nav>
    </Drawer>

    <div class="flex items-center p-4 bg-white" style="z-index:1;">
        <div class='text-black font-bold text-xl'>Programowanie zespołowe - zespół 8</div>
        <nav class="flex ms-auto lg:block hidden">
            <NavItem>Zespół</NavItem>
            <NavItem>Harmonogram</NavItem>
            <NavItem>Przebieg</NavItem>
            <NavItem>Raporty</NavItem>
            <NavItem>Dokumentacja</NavItem>
        </nav>
        <Button on:click={() => (navigationHidden = false)} class='lg:hidden ms-auto'>Nawigacja</Button>
        
    </div>

    <div class="grow">
        <div class="h-full relative">
            <img src='uplash-nurse.jpg' alt='nurse' class='h-full w-full object-cover absolute'>
            <div class="flex flex-col justify-center">
                <div class="text-slate-100 lg:py-32 py-6 lg:px-72 px-12" style="z-index:1;">
                    <div
                        class="bg-sky-300 text-black rounded-2xl p-10"
                    >
                        <span class="lg:text-9xl text-6xl font-light">MediCase</span
                        >
                        <div class="lg:text-3xl text-2xl py-2">
                            Nasza aplikacja służy do nauki treści medycznych oraz
                            umożliwia przeprowadzanie symulacji wywiadu z pacjentem
                            w wybranych językach, aktualnie polski oraz angielski.
                            Nauka obejmuje przegląd treści tekstowych, audio i video oraz testowanie zdobytej wiedzy.
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<style>

</style>
