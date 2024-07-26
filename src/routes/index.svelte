<script>
  import { onMount } from 'svelte';
  import Header from '../lib/Header.svelte';
  import ProductList from '../lib/ProductList.svelte';
  import { getProducts } from '../lib/api.js';

  let products = [];

  onMount(async () => {
    products = await getProducts();
  });
</script>

<Header title="My Online Shop" />
<ProductList {products} />

<style>
  main {
    padding: 1rem;
  }
</style>
