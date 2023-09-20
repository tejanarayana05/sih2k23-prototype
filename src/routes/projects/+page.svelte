<!-- src/routes/projects/App.svelte -->
<script>
    import Card from '../../components/Card.svelte';
  
    // Create an array of data for your cards (e.g., you can fetch this data from an API)
    let cards = [
      {
        id : 1,
        title: "Project 1 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "442",
        votes: "110"
      },
      {
        id : 2,
        title: "Project 2 Title",
        description: "Description for Card 2",
        image: "ProjectManagement.jpg",
        likes: "543",
        votes: "564"
      },
      {
        id : 3,
        title: "Project 3 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "456",
        votes: "65"
      },
      {
        id : 4,
        title: "Project 4 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "563",
        votes: "450"
      },
      {
        id : 5,
        title: "Project 5 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "98",
        votes: "430"
      },
      {
        id : 6,
        title: "Project 6 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "674",
        votes: "564"
      },
      {
        id : 7,
        title: "Project 7 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "765",
        votes: "562"
      }
      // Add more card data as needed
    ];
  </script>
  
  <main class="p-4">
    <div class="flex flex-wrap -mx-2 ">
      {#each cards as card (card.title)}
        <div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 px-2 mb-4">
          <Card
            id = {card.id}
            title={card.title}
            description={card.description}
            image={card.image}
            likes={card.likes}
            votes={card.votes}
          />
        </div>
      {/each}
    </div>
  </main>
  
  <style>
main {
    font-family: Space Grotesk;
    width: 100%;
    overflow: hidden;
  }  </style>