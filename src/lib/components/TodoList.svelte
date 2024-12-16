<script>
	let { todos, deleteTodo } = $props();
</script>

<ul class="todo__list">
	{#each todos as todo, i (todo.id)}
		<li class="todo__list__item">
			<label>
				<input
					bind:checked={todos[i].completed}
					type="checkbox"
					id="todo-{todo.id}"
					name="todo-{todo.id}"
				/>
				<span>{todo.title}</span>
			</label>
			<button onclick={() => deleteTodo(todo.id)} aria-label="Supprimer todo">
				<svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24">
					<path
						fill="none"
						stroke="currentColor"
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M3 6h18m-2 0v14c0 1-1 2-2 2H7c-1 0-2-1-2-2V6m3 0V4c0-1 1-2 2-2h4c1 0 2 1 2 2v2m-6 5v6m4-6v6"
					/>
				</svg>
			</button>
		</li>
	{/each}
</ul>
