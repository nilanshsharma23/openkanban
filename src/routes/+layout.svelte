<script lang="ts">
  import "./layout.css";
  import "remixicon/fonts/remixicon.css";

  let { children } = $props();
</script>

<div>
  {@render children()}
</div>
