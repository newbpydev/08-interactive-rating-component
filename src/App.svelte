<!-- * SCRIPT -->
<script lang="ts">
  // your script goes here

  import Attribution from "./components/Attribution.svelte";
  import InteractiveRating from "./components/InteractiveRating.svelte";
  import ThankYou from "./components/ThankYou.svelte";

  let rating: number;
  let maxRating: number = 5;
  let isRating = true;

  const handleRating = (valuation: number) => {
    rating = valuation;
    isRating = false;
  };
</script>

<!-- * TEMPLATE -->
<main>
  {#if isRating}
    <InteractiveRating {rating} {maxRating} setRating={handleRating} />
  {:else}
    <ThankYou {rating} {maxRating} />
  {/if}

  <!-- <Attribution /> -->
</main>

<!-- * STYLE -->
<style>
  main {
  }
</style>
