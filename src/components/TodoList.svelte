<script>
     import TodoItem from './TodoItem.svelte'
     export let todoItems  
     export let deleteTodo

</script>
       
<style>
    .todolist {
        margin: 2em;
    }
</style>

  <div class='todolist'>
    {#each todoItems as todo}
    <TodoItem todo={todo} onDelete={deleteTodo}/>
    {/each}
  </div>