<script>
    import { data } from "../finderStore";
    let input = '';

    const handleBtn = async () => {
        data.set([]); // Resetea la resp global
        let resp = await fetch(`https://api.giphy.com/v1/gifs/search?api_key=PyiReUyCFTIE4tBE7u31jrqZ4WsXtZbO&q=${input}&limit=10`);
        resp = await resp.json();
        
        data.update(o => resp["data"]);
        input = '';
    }
</script>

<form class="
        flex
        flex-col
        items-center
        my-10
        mx-4
        md:flex-row
        md:justify-center
        md:items-center
    "
    on:submit|preventDefault={handleBtn}
    >
    <input  class="
                w-
                border-b
                border-gray-400
                p-2
                mb-6
                md:mb-0
            "
            type="text"
            placeholder="Buscar Gif"
            bind:value={input}
            >
    
    <button class="
                bg-slate-500
                w-24
                py-2
                rounded-md
                text-white
                hover:bg-slate-800
                md:px-6
                md:ml-4
            "
            type="submit"
            >
            Buscar
    </button>
</form>