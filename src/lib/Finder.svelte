<script>
    import { data } from "../finderStore";
    let input = '';

    const handleBtn = async () => {
        let resp = await fetch(`https://api.giphy.com/v1/gifs/search?api_key=PyiReUyCFTIE4tBE7u31jrqZ4WsXtZbO&q=${input}`);
        resp = await resp.json();
        
        data.update(o => resp["data"]);
        console.log($data);

        input = '';
    }
</script>

<form class="
        flex
        flex-col
        items-center
        my-10
        mx-4
    "
    on:submit|preventDefault={handleBtn}
    >
    <input  class="
                border-b
                border-gray-400
                p-2
                mb-6
            "
            type="text"
            placeholder="Buscar Gif"
            bind:value={input}
            >
    
    <button class="
                bg-slate-500
                w-1/3
                py-2
                rounded-md
                text-white
                hover:bg-slate-800
            "
            type="submit"
            >
            Buscar
    </button>
</form>