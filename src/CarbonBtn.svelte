<script>
    export let name;
    export let kind;
    export let size;
    import { Button } from "carbon-components-svelte";
    export let handleClick;
</script>

<Button {kind} {size} on:click={handleClick}>{name}</Button>
