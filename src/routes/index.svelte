<script>
    import Finder from "../lib/Finder.svelte";
    import Card from "../lib/Card.svelte";

    // TODO: Crear los elementos globales de la Store
    import { data } from "../finderStore";

</script>

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
        <Card {gif} ></Card>
    {/each}
</div>