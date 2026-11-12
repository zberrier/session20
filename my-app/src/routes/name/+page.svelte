<script lang='ts'>
    let name = $state('');
</script>

<input type='text' bind:value={name}/>
<p>{name}</p>
