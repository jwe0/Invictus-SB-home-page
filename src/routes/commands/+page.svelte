<script lang="ts">
    import "/src/style.css";
    import { onMount } from 'svelte';


    interface Dependency {
        name: string;
        description: string;
        params: string[][];
        example: string;
        section: string;
        page: number;
    }

    let dependencies : Dependency[] = [];

    onMount(async () => {
        const res = await fetch('https://raw.githubusercontent.com/jwe0/Invictus-SB/main/modules/Dependencies/cmds.json');
        const data = await res.json();
        dependencies = Object.values(data);
    });
</script>
<head>
    <title>Invictus Selfbot</title>
</head>

<main>
    <div class="center3">
        <h1 class="title">Commands</h1>
        <h5 class="subtitle">Check out some of the commands</h5>
    </div>
    <table class="styled-table">
        <thead>
            <tr>
                <th>Name</th>
                <th>Description</th>
                <th>Params</th>
                <th>Example</th>
                <th>Section</th>
                <th>Page</th>
            </tr>
        </thead>
        <tbody>
            {#each dependencies as dependency}
                <tr>
                    <td>{dependency.name}</td>
                    <td>{dependency.description}</td>
                    <td>
                        <ul>
                            {#each dependency.params as param}
                                <li>{param[0]}: {param[1]}</li>
                            {/each}
                        </ul>
                    </td>
                    <td>{dependency.example}</td>
                    <td>{dependency.section}</td>
                    <td>{dependency.page}</td>
                </tr>
            {/each}
        </tbody>
    </table>
</main>
