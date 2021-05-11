<script lang="ts">
    import type { Product } from "../model/product";

    const productList: Product[] = [
        { id: '1', description: 'Filet de merluza', qty: 5 },
        { id: '2', description: 'Pata muslo', qty: 4 },
        { id: '3', description: 'Salsa', qty: '1 pote' },
        { id: '4', description: 'Rapiditas', qty:'1 bolsa'},
    ]

    let filteredProductList: Product[] = productList;
    let searchText: string;

    $: filteredProductList = searchText ? productList.filter(p => p.description.toLowerCase().startsWith(searchText.toLowerCase())) : productList;
</script>

<main>
<h1>Product list</h1>
    <form>
        <input type="search" placeholder="Buscar..." bind:value={searchText} />
    </form>
<ol>
    {#each filteredProductList as {description, qty }}
        <li>{description}: {qty}</li>
    {/each}
</ol>
</main>
