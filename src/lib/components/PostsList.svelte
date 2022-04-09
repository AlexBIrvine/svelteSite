<script>
	import PostCard from './PostCard.svelte'

	export let posts = []
</script>


<ul class="posts-list">
	{#each posts as post}
		<PostCard {post} class="post" />
	{/each}
</ul>

<style>
	.posts-list {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
		gap: 2.5%;
	}
</style>