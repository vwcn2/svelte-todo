<script>
    export let todo
    export let onDelete
</script>
    

<style>

</style>
<div class='todoitem'>
    {todo.id} - {todo.task} 
    <button on:click={onDelete(todo.id)}>Del</button>
</div>