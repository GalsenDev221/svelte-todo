<script>
	import TodoActions from '$lib/components/TodoActions.svelte';
	import TodoAdd from '$lib/components/TodoAdd.svelte';
	import TodoList from '$lib/components/TodoList.svelte';
	import '../app.css';

	let todos = $state([
		{ id: '1', title: 'Item #1', completed: true },
		{ id: '2', title: 'Item #2', completed: false }
	]);
	let remainingTodos = $derived(todos.filter((e) => !e.completed).length);

	// all - active - complete
	let filter = $state('all');
	let filteredTodos = $derived.by(() => {
		if (filter === 'all') {
			return todos;
		} else if (filter === 'active') {
			return todos.filter((e) => !e.completed);
		} else if (filter === 'completed') {
			return todos.filter((e) => e.completed);
		} else {
			return todos;
		}
	});

	function deleteTodo(id) {
		todos = todos.filter((e) => e.id !== id);
	}
</script>

<section>
	<h1>Todo App</h1>

	<article class="todo">
		<TodoAdd bind:todos />

		<TodoList {deleteTodo} todos={filteredTodos} />

		<TodoActions {remainingTodos} bind:filter />
	</article>
</section>
