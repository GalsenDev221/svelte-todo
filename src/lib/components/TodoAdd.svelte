<script>
	let { todos = $bindable() } = $props();

	function addTodo(e) {
		if (e.key !== 'Enter') {
			return;
		}

		todos.push({
			id: crypto.randomUUID(),
			title: e.target.value,
			completed: false
		});

		e.target.value = '';
	}
</script>

<header class="todo__header">
	<input onkeydown={addTodo} placeholder="Ajouter une todo" type="text" />
</header>
