<script lang="ts">
  let { text }: { text: String } = $props();

  let editMode = $state(false);

  let toggleEditMode = () => {
    editMode = !editMode;
  };
</script>

<div
  class="w-full p-2 flex flex-row bg-white rounded-lg text-xl justify-between items-center gap-2"
>
  {#if !editMode}
    <div>{text}</div>
  {:else}
    <input
      type="text"
      defaultValue={text}
      bind:value={text}
      id="input"
      class="w-full pl-2 rounded-lg"
      onsubmit={toggleEditMode}
      class:bg-gray-200={editMode}
    />
  {/if}
  <button
    class="p-1 hover:bg-gray-300 rounded-lg cursor-pointer"
    title="Edit"
    onclick={toggleEditMode}
  >
    <i class="ri-pencil-fill"></i>
  </button>
</div>
