<script>
    import { marked } from "marked";
    import { onMount } from "svelte";

    let markdownInput = '';
    $: renderedHTML = marked.parse(markdownInput);

</script>


<a href="/" class="fixed bottom-1 left-1 text-black">Go back</a>
<div class="w-screen h-screen bg-black flex text-white">
    <div class="flex w-full h-full">
        <div class="w-1/2 h-full bg-white flex">
            <textarea name="markdown-input" id="input" class="w-full h-full text-black p-10 font-mono" placeholder="Edit your markdown here..." bind:value={markdownInput}></textarea>
        </div>
        <div class="w-1/2 h-screen">
            <article class="h-full prose prose-headings:text-white max-w-none p-2 bg-zinc-800" id="preview">
                {@html renderedHTML}
            </article>
        </div>
        
    </div>
</div>

<style>
    textarea:focus {
        @apply appearance-none;
        @apply outline-none;
        @apply border-none;
    }

</style>