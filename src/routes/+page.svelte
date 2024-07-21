<script>
    import "/src/style.css";
    import { download } from "$lib/index";
</script>

<head>
    <title>Invictus Selfbot</title>
</head>


<body>
    <div class="top_bar">
        <div class="top_title">
            <h1 class="title">Invictus Selfbot</h1>    
            <h3>Like Nighty but free...</h3>
        </div>

        <div class="top_container">
            <button class="nav_button" on:click={() => window.location.href = download}>Download</button>
            <button class="nav_button" on:click={() => window.location.href = '/documentation'}>Documentation</button>
            <button class="nav_button" on:click={() => window.location.href = '/commands'}>Commands</button>
        </div>
    </div>

    <div class="center3">
        <h1 class="title">Features</h1><br>
        <h5 class="subtitle">Check out some of the features</h5>

        <div class="info_container">

            <div class="info_box slide_in_left">
                <h1 class="info_title">Giveaway sniper</h1>
                <p class="info_subtitle">Automatically join giveaways. Supports custom bots and button reactions not just emoji reactions.</p>
            </div>

            <div class="info_box slide_in_right">
                <h1 class="info_title">Nitro sniper</h1>
                <p class="info_subtitle">Automatically redeem nitro codes. Checks for and invalid code before redeeming to prevent rate limits.</p>
            </div>

        </div>  

        <div class="info_container">

            <div class="info_box slide_in_top">
                <h1 class="info_title">Open source</h1>
                <p class="info_subtitle">This entire project is fully open source and available on GitHub using the button above. Feel free to contribute.</p>
            </div>

        </div>

        <div class="info_container">

            <div class="info_box slide_in_left">
                <h1 class="info_title">Custom scripts</h1>
                <p class="info_subtitle">If you want to add functionallity your can do so using our custom scripting feature. Scripts are written in python and are easy to implement.</p>
            </div>

            <div class="info_box slide_in_right">
                <h1 class="info_title">Spoof</h1>
                <p class="info_subtitle">All requests sent to Discord are spoofed. These spoofed headers contain fake valid x-super-properties, cookies and much more.</p>
            </div>

        </div>

    </div>
</body>