<script>
    import Nav from '../../scripts/components/Nav.svelte';
    import Post1 from './post/2.svx';
    let spellcheck = !process.env.IS_PROD;
</script>

<main>
    <Nav />
    <div class="post" contenteditable={spellcheck} {spellcheck}>
        <Post1 />
    </div>
</main>

<style>
    main {
        margin: 0 auto;
        width: 90%;
    }
    .post {
        /* migsnote: update to real value */
        margin-left: auto;
        margin-right: auto;
        width: 85%;
    }
    /* migsnote: switch dark-mode back */
    /* :global(body) {
        background-color: #f2eee2;
        color: #0084f6;
        transition: background-color 0.3s;
    } */
    :global(body) {
        background-color: #1d3040;
        color: #d0d3d8;
    }
    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }
</style>
