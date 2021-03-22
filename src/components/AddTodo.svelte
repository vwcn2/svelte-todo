<script>
    let task
    export let addTodo
    const onAdd = () => {
        addTodo(task)
        task = ''
    }
</script>
<style>

</style>

<form on:submit|preventDefault={onAdd}>
        <input type='text' name='task' 
            bind:value={task}
            placeholder="new todo task" />
        <button>add</button>
</form>