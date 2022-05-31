<script>
    import { page } from '$app/stores';
    import { data } from "../finderStore";

    import Finder from "../lib/Finder.svelte";
    import Card from "../lib/Card.svelte";


</script>


<svelte:head>
  <title>{$page.stuff.title || 'Giphynder'}</title>
</svelte:head>

<Finder></Finder>

<div class="
        container
        w-11/12
        mx-auto
        grid
        grid-cols-1
        gap-6
        md:grid-cols-2
        lg:grid-cols-3
    ">
    {#each $data as gif}
        <Card title={gif.title} gifUrl={gif.images["fixed_height"].url} ></Card>
    {/each}
</div>