<script lang="ts">
  import TeammateCard from "./TeammateCard.svelte";
  import Timeline from "./Timeline.svelte";
  import TimelineItem from "./TimelineItem.svelte";
  import Pdf from "virtual:icons/mdi/file-pdf-box";
  import {teammates, harmonogram, progress, raports} from '../assets/data';

  
</script>

<div style="z-index:1;">
  <div class="bg-[#8EC2E0]">
    <div class="container mx-auto">
      <div class="flex justify-center text-6xl py-16">Nasz zespół</div>

      <div
        class="grid xl:grid-cols-3 md:grid-cols-2 grid-cols-1 lg:gap-12 md:gap-6 gap-3 lg:px-40 md:px-20 px-10"
      >
        {#each teammates as teammate}
          <TeammateCard {...teammate} />
        {/each}
      </div>
    </div>

    <div class="relative">
      <div class="w-full">
        <div class="container mx-auto">
          <div class="flex justify-center text-6xl py-16">Harmonogram</div>
          <Timeline>
            {#each harmonogram as item}
              <TimelineItem {...item} dotClass='bg-neutral-600'/>
            {/each}
          </Timeline>
        </div>
      </div>
    </div>
    <img src="wave2.svg" alt="" class='w-full object-cover'/>
  </div>

  <div class="bg-[#E090A1]">
    <div class="container mx-auto">
      <div class="flex justify-center text-6xl py-16">Przebieg prac</div>

      <Timeline>
        {#each progress as meeting}
          <TimelineItem {...meeting} dotClass='bg-neutral-600'/>
        {/each}
      </Timeline>
    </div>

    <div class="container mx-auto">
      <div class="flex justify-center text-6xl py-16">Raporty semestralne</div>

      <div
        class="grid xl:grid-cols-3 md:grid-cols-2 grid-cols-1 lg:gap-12 md:gap-6 gap-3 lg:px-40 md:px-20 px-10"
      >
        {#each raports as raport}
          <a
            href={raport.download}
            download={raport.download}
            class="flex flex-col items-center bg-slate-300 rounded-lg p-4"
          >
            <Pdf class="text-9xl" />
            {raport.name}
          </a>
        {/each}
      </div>
    </div>

    <div class="container mx-auto">
      <div class="flex justify-center text-6xl py-16">Dokumentacja</div>
    </div>
  </div>
</div>

