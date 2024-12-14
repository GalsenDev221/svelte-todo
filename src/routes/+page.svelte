<script>
	import '../app.css';
</script>

<section>
	<h1>Todo App</h1>

	<article class="todo">
		<!-- TODO: make this a component -->
		<header class="todo__header">
			<input placeholder="Ajouter une todo" type="text" />
		</header>

		<!-- TODO: make this a component -->
		<ul class="todo__list">
			<li class="todo__list__item">
				<label>
					<input type="checkbox" id="todo-1" name="todo-1" />
					<span>Apprendre Java<span style="font-size: var(--font-size-1)">(script)</span></span>
				</label>
				<button aria-label="Supprimer todo">
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
			<li class="todo__list__item">
				<label>
					<input checked type="checkbox" id="todo-2" name="todo-2" />
					<span>Apprendre Svelte</span>
				</label>
				<button aria-label="Supprimer todo">
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
		</ul>

		<footer class="todo__actions">
			<div class="todo__actions__remaining">0 todos restant</div>
			<div class="todo__actions__filter">
				<button class="active">Tout</button>
				<button>Terminé</button>
				<button>Actif</button>
			</div>
		</footer>
	</article>
</section>
