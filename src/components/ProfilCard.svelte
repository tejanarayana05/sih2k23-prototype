<!-- ProfileCard.svelte -->

<script>
    export let name;
    export let email;
    export let username;
    export let imageUrl; // Add a new prop for the image URL
   </script>
   
   <div class="bg-white rounded-lg shadow-lg p-4 text-center">
     <img src={imageUrl} alt="Profile Image" class="w-20 h-20 mx-auto rounded-full mb-4" />
     <h2 class="text-xl font-semibold">{name}</h2>
     <p class="text-gray-600">{email}</p>
     <p class="text-gray-600">@{username}</p>
   </div>
   