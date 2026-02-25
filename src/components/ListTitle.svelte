<script lang="ts">
  let title = $state("TODO");

  console.log("hi");
</script>

<input
  class="text-2xl text-black font-bold flex flex-row justify-between items-center gap-2 cursor-pointer w-full focus:bg-gray-300"
  bind:value={title}
  type="text"
  defaultValue={title}
/>
