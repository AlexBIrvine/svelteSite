<script>
  // import MainNav from './MainNav.svelte'
  import { siteAuthor } from '$lib/config'
</script>

<footer>
  <a href="/api/rss.xml" rel="external"><img src="/images/rss.png" alt="RSS logo"></a>
  <p>&copy;{new Date().getFullYear()} {siteAuthor}</p>
</footer>