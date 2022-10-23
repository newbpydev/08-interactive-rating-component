<!-- * SCRIPT -->
<script lang="ts">
  export let rating = 1;
</script>

<!-- * TEMPLATE -->
<article class="thank-you">
  <p class="thank-you__rating">You selected {rating} out of 5</p>

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
    padding: 3.4rem 2.4rem 3.7rem 2.4rem;
    text-align: center;
    display: flex;
    flex-direction: column;
  }

  .thank-you__rating {
  }

  .thank-you__heading {
  }

  .thank-you__message {
  }
</style>
