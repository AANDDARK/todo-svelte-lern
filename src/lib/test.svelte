<script>
    import { fade } from "svelte/transition";

    let value = $state(0)
    $effect(() => {
        setInterval(() => {
            value += 1
        }, 1000)    
    })
</script>

{#key value}
	<div transition:fade>{value}</div>
{/key}