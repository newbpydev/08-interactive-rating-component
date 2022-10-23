<!-- * SCRIPT -->
<script lang="ts">
  import starImg from "../assets/images/icon-star.svg";

  export let maxRating: number = 5;
</script>

<!-- * TEMPLATE -->
<article class="interactive-rating">
  <img
    src={starImg}
    class="interactive-rating__image"
    alt="An illustration of an orange star"
  />

  <h1 class="interactive-rating__heading">How did we do?</h1>

  <p class="interactive-rating__message">
    Please let us know how we did with your support request. All feedback is
    appreciated to help us improve our offering!
  </p>

  <div class="interactive-rating__rating-container">
    {#each Array(maxRating) as _, i (i)}
      <button class="interactive-rating__button-rating" type="button">
        {i + 1}
      </button>
    {/each}
  </div>

  <button class="interactive-rating__button" type="submit">Submit</button>
</article>

<!-- * STYLE -->
<style>
  .interactive-rating {
    max-width: 32.7rem;
    padding: 2.4rem 2.4rem 3.2rem 2.4rem;
    display: flex;
    flex-direction: column;
  }

  .interactive-rating__image {
    /* width: 1.396rem; */
    width: 4rem;
    padding: 1.302rem;
    background: var(--neut-blue-dark);
    border-radius: 50%;
  }

  .interactive-rating__heading {
  }

  .interactive-rating__rating-container {
  }

  .interactive-rating__rating {
  }

  .interactive-rating__button {
    cursor: pointer;
  }
</style>
