<script>

    import Card from '../../components/Card.svelte';
    import Profile from '../../components/Profile.svelte';

  let user = {
    // User data goes here
    username: 'john_doe',
    fullName: 'John Doe',
    email: 'john.doe@example.com',
    phone: '123-456-7890',
    address: '123 Main St, City, Country',
    college: 'Example University',
    branch: 'Computer Science',
    year: '2023',
    semester: 'Spring',
  };

    let cards = [
      {
        title: "Project 1 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "5622",
        votes: "154"
      },
      {
        title: "Project 1 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "123",
        votes: "170"
      },
      {
        title: "Project 1 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "412",
        votes: "1000"
      }
    ];
    let uploaded = [
      {
        title: "Project 1 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "5622",
        votes: "154"
      },
      {
        title: "Project 1 Title",
        description: "Description for Card 1",
        image: "ProjectManagement.jpg",
        likes: "123",
        votes: "170"
      }
    ];
</script>

<main class="p-4">
    <div>
        <p class="font-bold text-2xl mb-2">Profile</p>
    </div>
    <Profile {user} />
    <div>
        <p class="font-bold text-2xl mb-2">Uploaded Projects</p>
    </div>
    <div class="flex flex-wrap -mx-2">
        {#each uploaded as card (card.title)}
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
    <div>
        <p class="font-bold text-2xl mb-2">Liked Projects</p>
    </div>
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
  </main>
  