<script>
    export let post;
</script>



<!-- {#each posts as post} -->

<li class="card">
    <a href="/blog/{post.slug}">
    <article>
        <p>{post.date}</p>
        <h2>{post.title}</h2>
    </article>
    
    <p class="excerpt">{post.excerpt}</p>

    {#if post.categories}
    <aside class="category-list">
        <ul>
            {#each post.categories as category}
            <li>
                <a href="/blog/category/{category}/">
                    { category }
                </a>
            </li>
            {/each}
        </ul>
    </aside>
    {/if}
</a>
</li>


<style>
    .card {
        margin: 25px 0;
        background-color: #121212;    /* Maybe revist this color */
        color: #D8DEE9;
        border-radius: 20px 50px;
        padding: 20px 5%;
    }

    article{
        color: #D8DEE9;
    }

    a {
        text-decoration: none;
    }

    .excerpt {
        padding-bottom: 10px;
    }

    .category-list li {
        margin:0;
    }

    .category-list ul {
        padding: 0;
        display: flex;
        flex-direction: column;
    }

    .category-list li {
        display: inline-block;
        font-size: 0.8rem;
        margin: 0 2rem;
    }

    .category-list li a {
        background-color: #5E81AC;
        color: #D8DEE9;
        padding: .5rem 0.75rem;
        margin-bottom: 1rem;
        text-transform: uppercase;
        text-align: center;
        font-weight: bold;
    }

    h2 {
        margin-top: 0;
    }

    p {
        color: #D8DEE9;
        margin:0;
        text-decoration: none;
    }

    @media screen and (min-width: 768px) {
        .category-list ul {
            flex-direction: row;
            padding-top: 5px;
        }
        .category-list li {
            margin: 0;
            margin-right: 1rem;
        }
    }
    
</style>