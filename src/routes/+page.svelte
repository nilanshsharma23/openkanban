<script lang="ts">
  import List from "../components/List.svelte";

  const items1 = [
    {
      name: "Hello",
      id: 1,
    },
    {
      name: "Hello2",
      id: 2,
    },
    {
      name: "Hello3",
      id: 3,
    },
    {
      name: "Hello4",
      id: 4,
    },
  ];

  const items2 = [
    {
      name: "Hello2",
      id: 1,
    },
    {
      name: "Hello22",
      id: 2,
    },
    {
      name: "Hello23",
      id: 3,
    },
    {
      name: "Hello24",
      id: 4,
    },
  ];
</script>

<div class="h-screen w-screen flex flex-col justify-center not-last p-8 gap-4">
  <div class="text-4xl text-white font-bold">Board Title</div>
  <div class="flex flex-row items-center justify-start h-full w-full gap-4">
    <List items={items1} />
    <List items={items2} />
  </div>
</div>
