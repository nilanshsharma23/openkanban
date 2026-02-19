<script lang="ts">
  let editMode = $state(false);
  let title = $state("TODO");

  let focusIn = () => {
    editMode = true;
    console.log("here");
  };

  let focusOut = () => {
    editMode = false;
    console.log("nothere");
  };
</script>

<div
  class="text-2xl text-black font-bold flex flex-row justify-between items-center gap-2 cursor-pointer"
  class:bg-grey-200={editMode}
>
  <input
    type="text"
    defaultValue={title}
    class="w-full"
    onfocusin={focusIn}
    onfocusout={focusOut}
  />
</div>
