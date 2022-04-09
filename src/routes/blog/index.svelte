<script context="module">
	export const load = async ({ fetch }) => {
		const postRes = await fetch(`/api/posts.json`)
		const { posts } = await postRes.json()

		let uniqueCategories = {}

		posts.forEach(post => {
			post.categories.forEach(category => {
				if (uniqueCategories.hasOwnProperty(category)) {
					uniqueCategories[category].count += 1
				} else {
					uniqueCategories[category] = {
						title: category,
						count: 1
					}
				}
			})
		})

		const totalRes = await fetch(`/api/posts/count.json`)
		const { total } = await totalRes.json()
		
		const sortedUniqueCategories = 
			Object.values(uniqueCategories)
				.sort((a, b) => a.title < b.title)

		return {
			props: { posts, total, sortedUniqueCategories }
		}
	}
</script>



<script>
	import PostsList from '$lib/components/PostsList.svelte'
	import Pagination from '$lib/components/Pagination.svelte'
	import Sidebar from '$lib/components/Sidebar-Categories.svelte'
	import { siteDescription } from '$lib/config'
	export let posts
	export let total
	export let sortedUniqueCategories
</script>


<svelte:head>
	<title>Blog</title>
	<meta data-key="description" name="description" content={siteDescription}>
</svelte:head>


<h1>Blog</h1>

<div id="main-window">
	<Sidebar {sortedUniqueCategories} ref="Sidebar"/>
	<PostsList {posts} ref="PostsList" />
</div>

<Pagination currentPage={1} totalPosts={total} />


<style>
	#main-window {
		height: 100%;
		display: grid;
		grid-template-columns: 1fr 4fr;
		column-gap: 5%;
	}

	/* :global([ref=Sidebar]) {
		background-color: pink;
	} */


</style>