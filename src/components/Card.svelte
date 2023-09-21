<!-- src/components/Card.svelte -->
<script>
  export let id ;
  export let title;
  export let description;
  export let image;
  export let likes;
  export let votes;
</script>

<div class="max-w-md rounded overflow-hidden shadow-lg">
  <img class="w-full" src={image} alt={title}>
  <div class="px-6 py-4">
    <div class="font-bold text-xl mb-2">{title}</div>
    <p class="text-gray-700 text-base">{description}</p>
  </div>
  <div class="px-6 py-4">
    <span class="inline-block  rounded-full px-3 py-1 text-sm font-semibold text-gray-700 mr-2">
      ❤️ {likes}
    </span>
    <span class="inline-block  rounded-full px-3 py-1 text-sm font-semibold text-gray-700">
      ⬆ {votes}
    </span>
  </div>
  <div class="px-6 py-4">
    <a href="/projects/{id}">
      <button
      class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
    >
      Click to View
    </button>
    </a>
    
  </div>
</div>
