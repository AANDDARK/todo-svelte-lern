<script>
import { todos } from "../todos.svelte";

let name = ''
let text = ''
const save = () => {
    todos.update(item => [...item, {
        id: 0 + item.length,
        name,
        text
    }])

    name = '';
    text = '';
}
console.log($todos);

const clear = () => {
    todos.set([])
}
</script>


<div>
        <input bind:value={name} placeholder="Name" />
        <textarea bind:value={text} placeholder="Text"></textarea>
        <button on:click={save}>Save</button>
      <button on:click={clear}>clear</button>  
</div>

