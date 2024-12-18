<script>
    import "../app.css";
    import {page} from "$app/stores"


    const navigation = [
        {
            label:"Home",
            src:"/"
        },
        {
            label:"Upload",
            src:"/upload"
        },
        {
            label:"Reels",
            src:"/reels"
        },
        {
            label:"Profile",
            src:"/my-profile"
        },
    ]

</script>
    
<slot />

<div class="flex flex-row items-center justify-evenly fixed bottom-0 bg-white border border-white border-t-black">

    {#each navigation as item}

    <div class= "p-6">

        {#if $page.url.pathname == item.src}

            <a href={item.src} class="font-bold">{item.label}</a>

            {:else}

            <a href={item.src}>{item.label}</a>
            
        {/if}

    </div>
        
    {/each}

</div>