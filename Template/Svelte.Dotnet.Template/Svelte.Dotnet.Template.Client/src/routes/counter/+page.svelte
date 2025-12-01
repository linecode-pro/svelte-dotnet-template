<script>
  import PageTitle from '../components/PageTitle.svelte';

  let currentCount = $state(0);

  function incrementCount() {
    currentCount++;
  }
</script>

<PageTitle>Counter</PageTitle>

<h1>Counter</h1>

<p role="status">Current count: {currentCount}</p>

<button class="btn btn-primary" onclick={incrementCount}>Click me</button>