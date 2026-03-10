<script lang="ts">
  import ListItem from "./ListItem.svelte";
  import ListTitle from "./ListTitle.svelte";
  import { dndzone } from "svelte-dnd-action";

  let { items }: { items: { name: String; id: Number }[] } = $props();

  function handleDndConsiderItems(e: any) {
    console.log(e);
  }

  function handleDndFinalizeItems(e: any) {
    items = e.detail.items;
  }
</script>

<div
  class="w-64 h-full bg-gray-200 opacity-80 flex flex-col rounded-3xl p-4 gap-4"
>
  <ListTitle />
  <div
    class="w-full h-full flex flex-col gap-2"
    use:dndzone={{ items }}
    onconsider={(e) => handleDndConsiderItems(e)}
    onfinalize={(e) => handleDndFinalizeItems(e)}
  >
    {#each items as item}
      <ListItem text={item.name} />
    {/each}
  </div>
</div>
