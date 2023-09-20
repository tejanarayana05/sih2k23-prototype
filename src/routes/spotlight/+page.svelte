<script>
  import Card from "../../components/Card.svelte";
  import ProfileCard from "../../components/ProfilCard.svelte";

  let cards = [
    {
      title: "Project 1 Title",
      description: "Description for Card 1",
      image: "ProjectManagement.jpg",
      likes: "5622",
      votes: "154",
    },
    {
      title: "Project 1 Title",
      description: "Description for Card 1",
      image: "ProjectManagement.jpg",
      likes: "123",
      votes: "170",
    },
    {
      title: "Project 1 Title",
      description: "Description for Card 1",
      image: "ProjectManagement.jpg",
      likes: "412",
      votes: "1000",
    },
  ];
  let profiles = [
    {
      name: "John Doe",
      email: "johndoe@gmail.com",
      username: "johndoe123",
      imageUrl: "user-profile.png", // Add the image URL
    },
    {
      name: "Jane Smith",
      email: "janesmith@gmail.com",
      username: "janesmith456",
      imageUrl: "user-profile.png", // Add the image URL
    },
    {
      name: "Bob Johnson",
      email: "bjohnson@gmail.com",
      username: "bob123",
      imageUrl: "user-profile.png", // Add the image URL
    },
  ];
  let technologies = [
    {
      name: "Blockchain",
      imageUrl: "blockchain.jpeg", // Replace with the actual image URL
    },
    {
      name: "Machine Learning (ML)",
      imageUrl: "ml.png", // Replace with the actual image URL
    },
    {
      name: "Deep Learning (DL)",
      imageUrl: "dl.jpg", // Replace with the actual image URL
    },
    {
      name: "Artificial Intelligence (AI)",
      imageUrl: "ai.jpeg", // Replace with the actual image URL
    },
  
    // Add more technologies as needed
  ];
</script>

<main class="p-4">
  <h1 class="text-center italic font-bold text-4xl mb-2">Spotlight</h1>
  <div>
    <br>
    <p class="p-4 font-bold text-2xl mb-2">Top Projects</p>
    <div class="flex flex-wrap -mx-2">
      {#each cards as card (card.title)}
        <div class="w-full md:w-1/2 lg:w-1/3 xl:w-1/4 px-2 mb-4">
          <Card
            title={card.title}
            description={card.description}
            image={card.image}
            likes={card.likes}
            votes={card.votes}
          />
        </div>
      {/each}
    </div>
  </div>
<br>
  <div>
    <p class="p-4 font-bold text-2xl mb-2">Top Contributors</p>
    <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
      {#each profiles as profile (profile.email)}
        <ProfileCard
          name={profile.name}
          email={profile.email}
          username={profile.username}
          imageUrl={profile.imageUrl}
        />
      {/each}
    </div>
  </div>
  <br>
  <div>
    <h1 class="p-4 font-bold text-2xl mb-2">Top Technologies</h1>
    <ul class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
      {#each technologies as tech (tech.name)}
        <li class="text-center">
          <img
            src={tech.imageUrl}
            alt={tech.name}
            class="w-24 h-24 mx-auto mb-2"
          />
          <p class="font-semibold">{tech.name}</p>
        </li>
      {/each}
    </ul>
  </div>
  <br>
</main>
