<script>
    import Nav from "../lib/components/Nav.svelte";
    import NoteContainer from "../lib/components/NoteContainer.svelte";
</script>



<div class="w-screen h-screen flex flex-col">
    <Nav />
    <NoteContainer />
</div>


<style>
    :global(body) {
        @apply bg-indigo-700;
    }
</style>
