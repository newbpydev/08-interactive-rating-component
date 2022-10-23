<!-- * SCRIPT -->
<script lang="ts">
  import starImg from "../assets/images/icon-star.svg";

  export let maxRating: number = 5;
  export let rating: number | null;
  export let setRating: (rating: number) => void;

  $: activeRating = rating - 1;

  const toggleRating = (e: MouseEvent) => {
    const target = e.target as HTMLInputElement;
    rating = parseInt(target.value);
  };

  const handleSubmit = (e: MouseEvent) => {
    setRating(rating);
    console.log(e.target);
  };
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
      <input
        class={`interactive-rating__rating ${
          activeRating === i ? "active" : ""
        }`}
        on:click={toggleRating}
        type="button"
        value={i + 1}
      />
    {/each}
  </div>

  <button
    class="interactive-rating__button"
    type="submit"
    on:click|preventDefault={handleSubmit}>Submit</button
  >
</article>

<!-- * STYLE -->
<style>
  .interactive-rating {
    max-width: 32.7rem;
    height: 36rem;
    padding: 2.4rem 2.4rem 3.2rem 2.4rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    /* align-items: center; */

    background: radial-gradient(
      98.96% 98.96% at 50% 0%,
      #232a34 0%,
      #181e27 100%
    );
    border-radius: var(--border-radius);
  }

  .interactive-rating__image {
    width: 4rem;
    padding: 1.302rem;
    background: var(--neut-blue-dark);
    border-radius: 50%;
    /* margin-bottom: 1.6rem; */
  }

  .interactive-rating__heading {
    font-weight: 700;
    font-size: 2.4rem;
    color: var(--neut-white);
    /* line-height: 3; */
    /* margin-bottom: 1rem; */
  }

  .interactive-rating__message {
    line-height: 157%;
    font-size: 1.4rem;
    /* margin-bottom: 2.4rem; */
  }

  .interactive-rating__rating-container {
    display: flex;
    justify-content: space-between;
  }

  .interactive-rating__rating {
    width: 4.2rem;
    height: 4.2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background: var(--neut-blue-dark);
    border-radius: 50%;
    cursor: pointer;
    transition: all 0.3s ease;
    color: var(--neut-grey-medium);
    /* margin-bottom: 2.4rem; */
  }

  .interactive-rating__rating.active {
    background: var(--neut-grey-medium);
    color: var(--neut-white);
  }
  .interactive-rating__rating:hover {
    background: var(--pri-orange);
    color: var(--neut-white);
  }

  .interactive-rating__button {
    cursor: pointer;
    border-radius: 5rem;
    height: 4.5rem;
    background: var(--pri-orange);
    color: var(--neut-white);
    text-align: center;
    transition: all 0.3s ease;
    letter-spacing: 0.186667rem;
    font-weight: 700;
    font-size: 1.4rem;
  }
  .interactive-rating__button:hover {
    background: var(--neut-white);
    color: var(--pri-orange);
  }

  /* * Media 1440 px = 90em  */
  @media (min-width: 90em) {
    .interactive-rating {
      max-width: 41.2rem;
      height: 41.6rem;
      border-radius: 3rem;
    }

    .interactive-rating__image {
      width: 4.8rem;
      padding: 1.6rem;
      margin-bottom: 1.5rem;
    }

    .interactive-rating__heading {
      font-size: 2.8rem;
    }

    .interactive-rating__message {
      line-height: 1.9;
      font-size: 1.5rem;
    }

    .interactive-rating__rating-container {
      margin-bottom: 1.5rem;
    }

    .interactive-rating__rating {
      width: 5.1rem;
      height: 5.1rem;
      font-size: 1.6rem;
    }

    .interactive-rating__button {
      letter-spacing: 0.2rem;
      font-size: 1.5rem;
      /* height: ; */
    }
  }
</style>
