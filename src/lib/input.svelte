<script>
import { todos } from "../todos.svelte";

let name = ''
let text = ''
const save = (event) => {
    event.preventDefault();
    todos.update(item => [...item, {
        name,
        text
    }])

    name = '';
    text = '';
}
$inspect($todos)
</script>


<div>
    <form on:submit={save}>
        <input bind:value={name} placeholder="Name" />
        <textarea bind:value={text} placeholder="Text"></textarea>
        <button type="submit">Save</button>
      </form>   
</div>

