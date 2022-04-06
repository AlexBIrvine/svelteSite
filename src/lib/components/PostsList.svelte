<script>
  import PostCard from './PostCard.svelte'

  export let posts = []
</script>


<ul class="posts-list">
  {#each posts as post}
    <PostCard {post}/>
  {/each}
</ul>

