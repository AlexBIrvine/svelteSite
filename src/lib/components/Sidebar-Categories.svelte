<script>
	export let sortedUniqueCategories
	export let ref
</script>



<aside id="sidebar" {ref}>
		<ul>
			{#each sortedUniqueCategories as category}
			<li class="category">
				<a href="/blog/category/{category.title}"> 
					<div>{ category.title } </div> 
					<div>{category.count}</div>
				</a>
			</li>
			{/each}
		</ul>
</aside>



<style>
	#sidebar {
		height: 100%;
	}

	#sidebar ul {
		display: flex;
		flex-direction: column;
		width: 90%;
	}

	.category {
		display: inline-block;
		font-size: 0.6rem;
		background-color: #5E81AC;
		color: #D8DEE9;
		padding: .5rem 0.75rem;
		margin-bottom: 1rem;
		text-transform: uppercase;
		text-align: center;
		font-weight: bold;
	}

	.category a {
		color: #D8DEE9;
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		text-decoration: none;
	}

</style>