<script>
    let catFacts = $state([]);

    async function newFact() {
        const res = await fetch('https://catfact.ninja/fact');
        if (res.ok) {
            const data = await res.json();
            catFacts.push(data.fact);
        } else {
            alert('it broke');
        }
    }
</script>

<h1>Cat Facts</h1>
<ul>
{#each catFacts as fact}
    <li>{fact}</li>
{/each}
</ul>
<button onclick={newFact}>more facts</button>
