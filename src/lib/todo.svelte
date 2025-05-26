<script>
    import { todos } from "../todos.svelte";

  let props = $props()
</script>

<div>
  <h1>{ props.name }</h1>
  <p> {props.text} </p>
  <button on:click={(() => todos.update(item => item.filter(item => item.id !== props.id)))}>remove</button>
</div>