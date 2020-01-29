<script>
  let weights = [
    "font-hairline",
    "font-thin",
    "font-light",
    "font-normal",
    "font-medium",
    "font-semibold",
    "font-bold",
    "font-extrabold",
    "font-black"
  ];
</script>

{#each weights as weight}
  <div class="mt-4">
    <span class="bg-gray-800 text-white rounded px-2 py-1">
      {weight.substring(5)}
    </span>
    <p class={weight}>
      Apparently we had reached a great height in the atmosphere, for the sky
      was a dead black, and the stars had ceased to twinkle. By the same
      illusion which lifts the horizon of the sea to the level of the spectator
      on a hillside, the sable cloud beneath was dished out, and the car seemed
      to float in the middle of an immense dark sphere, whose upper half was
      strewn with silver. Looking down into the dark gulf below, I could see a
      ruddy light streaming through a rift in the clouds.
    </p>
  </div>
{/each}
