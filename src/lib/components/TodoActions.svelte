<script>
	let { filter = $bindable(), remainingTodos } = $props();
</script>

<footer class="todo__actions">
	<div class="todo__actions__remaining">{remainingTodos} todos restant</div>
	<div class="todo__actions__filter">
		<button class:active={filter === 'all'} onclick={() => (filter = 'all')}> Tout </button>
		<button class:active={filter === 'active'} onclick={() => (filter = 'active')}>Actif</button>
		<button class:active={filter === 'completed'} onclick={() => (filter = 'completed')}>
			Terminé
		</button>
	</div>
</footer>
