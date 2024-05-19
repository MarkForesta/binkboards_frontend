<script>
	import {tournament} from "$lib/sample"
	import { Result } from "postcss";
	console.log(tournament)
    let width;
</script>

<div class="card">
    <header class="card-header p-4 text-center text-2xl fond-bold">
        {tournament.name}
    </header>
    <section>
        <table class="table">
            <thead>
                <tr>
                    <th>Player</th>
                    <th>Region</th>
                    <th>Date</th>
                    <th>Finish</th>
                </tr>
            </thead>
            <tbody>
                {#each tournament.tResult as result}
                    <tr>
                        <td>{result.name}</td>
                        <td>PA</td>
                        <td>{result.date}</td>
                        <td>{result.place}</td>
                    </tr>
                {/each}
            </tbody>
        </table>
    </section>
</div>

