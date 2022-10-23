<!-- * SCRIPT -->
<script lang="ts">
  // your script goes here

  import Attribution from "./components/Attribution.svelte";
  import InteractiveRating from "./components/InteractiveRating.svelte";
  import ThankYou from "./components/ThankYou.svelte";
</script>

<!-- * TEMPLATE -->
<main>
  <InteractiveRating />

  <ThankYou />

  <Attribution />
</main>

<!-- * STYLE -->
<style>
  main {
  }
</style>
