<script>
    import TodoList from './TodoList.svelte'
    import AddTodo from './AddTodo.svelte'

    let todoItems = []
    let newTodo = ''

    const addTodo = (task)=> {
        const todo = {
            task,
            id: todoItems.length
        }
        todoItems = [...todoItems, todo]
        console.log(todoItems)
    }
    const deleteTodo = (id) => {
        console.log("delete todo " +id)
        todoItems = todoItems.filter( item => item.id !== Number(id))
    }
</script>
<style>

</style>

<h3>Todoist App</h3>
<AddTodo addTodo={addTodo}/>
<TodoList todoItems={todoItems} deleteTodo={deleteTodo}/>