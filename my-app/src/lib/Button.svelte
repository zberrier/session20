<script lang='ts'>
    let count: number = $state(0);
    let props = $props();
    let highestClickCounter: number = $state(0);

    function addCount() {
        if (props.max > count) {
            count += 1;
            if (highestClickCounter < count) {
                highestClickCounter = count;
            }
        } else {
            alert('reached max count');
        }
    }

    function resetCount() {
        count = 0;
    }
</script>

<button onclick={addCount}>Click me!</button>
<button onclick={resetCount}>Reset Counter</button>
<p>{props.name}: {count}</p>
<p>Highest click count: {highestClickCounter}</p>
