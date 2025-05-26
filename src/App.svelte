<script>
    import Input from "./lib/input.svelte";
    import Test from "./lib/test.svelte";
    import Todo from "./lib/todo.svelte";
  import { todos } from "./todos.svelte";

  
</script>

<main>
  <Input />
  {#each $todos as todo}
      <Todo name={todo.name}, text={todo.text} id={todo.id}/>
  {/each}

  <hr />
  <Test />
</main>

