<script lang="ts">
  import List from "../components/List.svelte";
  import ListTitle from "../components/ListTitle.svelte";
</script>

<div class="h-screen w-screen flex flex-col justify-center not-last p-8 gap-4">
  <div class="text-4xl text-white font-bold">Board Title</div>
  <div class="flex flex-row items-center justify-start h-full w-full gap-4">
    <List />
  </div>
</div>
