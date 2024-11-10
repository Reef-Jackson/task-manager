<script>
    export let title;
    export let bulk;
</script>

<a href="/editor" class="w-full drop-shadow-md flex bg-white rounded hover:scale-[1.01] hover:cursor-pointer transition-transform">
    <span class="h-full bg-indigo-300 rounded-l p-2">{title}</span>
    <span class="h-full grow bg-indigo-400 rounded-r p-2">{bulk}</span>
</a>