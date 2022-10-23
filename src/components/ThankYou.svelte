<!-- * SCRIPT -->
<script lang="ts">
  import illusThankYou from "../assets/images/illustration-thank-you.svg";

  export let rating = 1;
  export let maxRating = 5;
</script>

<!-- * TEMPLATE -->
<article class="thank-you">
  <img
    class="thank-you__img"
    src={illusThankYou}
    alt="thank you illustration"
  />

  <p class="thank-you__rating">You selected {rating} out of {maxRating}</p>

  <h1 class="thank-you__heading">Thank you!</h1>

  <p class="thank-you__message">
    We appreciate you taking the time to give a rating. If you ever need more
    support, don't hesitate to get in touch!
  </p>
</article>

<!-- * STYLE -->
<style>
  .thank-you {
    max-width: 32.7rem;
    height: 36rem;
    padding: 3.4rem 2.4rem 3.7rem 2.4rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
    text-align: center;
    background: radial-gradient(
      98.96% 98.96% at 50% 0%,
      #232a34 0%,
      #181e27 100%
    );
    border-radius: var(--border-radius);
  }

  .thank-you__img {
    width: 14.4rem;
    margin: 0 auto;
  }

  .thank-you__rating {
    background: var(--neut-blue-dark);
    border-radius: 2.25rem;
    height: 3.2rem;
    width: 16.8rem;
    display: flex;
    justify-content: center;
    align-items: center;

    color: var(--pri-orange);
    font-size: 1.4rem;
    margin-bottom: 1rem;
    /* line-height: 157%; */
  }

  .thank-you__heading {
    color: var(--neut-white);
    font-weight: 700;
    font-size: 2.4rem;
    /* line-height: 3; */
  }

  .thank-you__message {
    font-size: 1.4rem;
    line-height: 1.5;
  }
</style>
