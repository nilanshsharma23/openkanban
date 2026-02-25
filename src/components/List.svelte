<script lang="ts">
  import ListItem from "./ListItem.svelte";
  import ListTitle from "./ListTitle.svelte";
</script>

<div
  class="w-64 h-full bg-gray-200 opacity-80 flex flex-col rounded-3xl p-4 gap-4"
>
  <ListTitle />
  <ListItem text="Hello" />
</div>
