<script>
    /** @type {import('./$types').PageData} */
    import { page } from "$app/stores";

    let cards = [
        {
            id: 1,
            title: "Project 1 Title",
            description: "Description for Card 1",
            image: 
                "https://s3-ap-south-1.amazonaws.com/static.awfis.com/wp-content/uploads/2017/07/07184649/ProjectManagement.jpg",
            likes: "442",
            votes: "110",
            technologies: ["React", "Node.js", "MongoDB"],
            contributors: ["John Doe", "Jane Smith"],
            documents: [
                {
                    name: "Project Document 1",
                    url: "https://example.com/doc1.pdf",
                },
                {
                    name: "Project Document 2",
                    url: "https://example.com/doc2.pdf",
                },
            ],
            folders: ["Code Folder 1", "Code Folder 2"],
        },
        {
            id: 2,
            title: "Project 2 Title",
            description: "Description for Card 2",
            image: "https://s3-ap-south-1.amazonaws.com/static.awfis.com/wp-content/uploads/2017/07/07184649/ProjectManagement.jpg",
            likes: "543",
            votes: "564",
            technologies: ["Angular", "Express.js", "MySQL"],
            contributors: ["Alice Johnson", "Bob Wilson"],
            documents: [
                {
                    name: "Project Document 3",
                    url: "https://example.com/doc3.pdf",
                },
                {
                    name: "Project Document 4",
                    url: "https://example.com/doc4.pdf",
                },
            ],
            folders: ["Code Folder 3", "Code Folder 4"],
        },
        {
            id: 3,
            title: "Project 3 Title",
            description: "Description for Card 3",
            image: "https://s3-ap-south-1.amazonaws.com/static.awfis.com/wp-content/uploads/2017/07/07184649/ProjectManagement.jpg",
            likes: "456",
            votes: "65",
            technologies: ["Vue.js", "Node.js", "MongoDB"],
            contributors: ["Eva Brown", "David Lee"],
            documents: [
                {
                    name: "Project Document 5",
                    url: "https://example.com/doc5.pdf",
                },
                {
                    name: "Project Document 6",
                    url: "https://example.com/doc6.pdf",
                },
            ],
            folders: ["Code Folder 5", "Code Folder 6"],
        },
        {
            id: 4,
            title: "Project 4 Title",
            description: "Description for Card 4",
            image: "https://s3-ap-south-1.amazonaws.com/static.awfis.com/wp-content/uploads/2017/07/07184649/ProjectManagement.jpg",
            likes: "563",
            votes: "450",
            technologies: ["React Native", "Firebase"],
            contributors: ["Michael Smith", "Sophia Clark"],
            documents: [
                {
                    name: "Project Document 7",
                    url: "https://example.com/doc7.pdf",
                },
                {
                    name: "Project Document 8",
                    url: "https://example.com/doc8.pdf",
                },
            ],
            folders: ["Code Folder 7", "Code Folder 8"],
        },
        {
            id: 5,
            title: "Project 5 Title",
            description: "Description for Card 5",
            image: "https://s3-ap-south-1.amazonaws.com/static.awfis.com/wp-content/uploads/2017/07/07184649/ProjectManagement.jpg",
            likes: "98",
            votes: "430",
            technologies: ["Python", "Django", "PostgreSQL"],
            contributors: ["Oliver Taylor", "Emily Davis"],
            documents: [
                {
                    name: "Project Document 9",
                    url: "https://example.com/doc9.pdf",
                },
                {
                    name: "Project Document 10",
                    url: "https://example.com/doc10.pdf",
                },
            ],
            folders: ["Code Folder 9", "Code Folder 10"],
        },
        {
            id: 6,
            title: "Project 6 Title",
            description: "Description for Card 6",
            image: "https://s3-ap-south-1.amazonaws.com/static.awfis.com/wp-content/uploads/2017/07/07184649/ProjectManagement.jpg",
            likes: "674",
            votes: "564",
            technologies: ["Ruby on Rails", "SQLite"],
            contributors: ["Sophie Brown", "James Wilson"],
            documents: [
                {
                    name: "Project Document 11",
                    url: "https://example.com/doc11.pdf",
                },
                {
                    name: "Project Document 12",
                    url: "https://example.com/doc12.pdf",
                },
            ],
            folders: ["Code Folder 11", "Code Folder 12"],
        },
        {
            id: 7,
            title: "Project 7 Title",
            description: "Description for Card 7",
            image: "https://s3-ap-south-1.amazonaws.com/static.awfis.com/wp-content/uploads/2017/07/07184649/ProjectManagement.jpg",
            likes: "765",
            votes: "562",
            technologies: ["Java", "Spring Boot", "MySQL"],
            contributors: ["Daniel Lee", "Lucy Smith"],
            documents: [
                {
                    name: "Project Document 13",
                    url: "https://example.com/doc13.pdf",
                },
                {
                    name: "Project Document 14",
                    url: "https://example.com/doc14.pdf",
                },
            ],
            folders: ["Code Folder 13", "Code Folder 14"],
        },
    ];

    


    let curr_project_id = $page.params.slug;

    let data = null; // Initialize data as null

    // Loop through the cards to find the matching card
    for (let i = 0; i < cards.length; i++) {
        if (cards[i].id === +curr_project_id) {
            // Use '+' to convert curr_project_id to a number
            data = cards[i];
            break; // Exit the loop once a match is found
        }
    }
</script>

<!-- Display data if it exists -->
{#if data}
<div class="container mx-auto mt-10 p-5">
    <div class="bg-white rounded-lg shadow-lg overflow-hidden">
        <img src={data.image} alt="{data.title}" class="w-full h-64 object-cover" />
        <div class="px-6 py-4">
            <h1 class="text-2xl font-semibold text-gray-800 mb-2">{data.title}</h1>
            <p class="text-gray-600 mb-4">{data.description}</p>
            <div class="flex items-center space-x-4">
                <div class="flex items-center">
                    <span class="text-gray-600">❤️{data.likes} Likes</span>
                </div>
                <div class="flex items-center">
                    <span class="text-gray-600">⬆️{data.votes} Votes</span>
                </div>
            </div>
            <div class="mt-4">
                <h2 class="text-lg font-semibold text-gray-800">Technologies Used:</h2>
                <ul class="list-disc list-inside mt-2">
                    {#each data.technologies as tech}
                        <li class="text-gray-600">{tech}</li>
                    {/each}
                </ul>
            </div>
            <div class="mt-4">
                <h2 class="text-lg font-semibold text-gray-800">Contributors:</h2>
                <ul class="list-disc list-inside mt-2">
                    {#each data.contributors as contributor}
                        <li class="text-gray-600">{contributor}</li>
                    {/each}
                </ul>
            </div>
        </div>
        <div class="px-6 py-4">
            <h2 class="text-lg font-semibold text-gray-800">Documents:</h2>
            <ul class="list-disc list-inside mt-2">
                {#each data.documents as doc}
                    <li class="text-blue-500 hover:underline"><a href="{doc.url}" target="_blank">{doc.name}</a></li>
                {/each}
            </ul>
        </div>
        <div class="px-6 py-4">
            <h2 class="text-lg font-semibold text-gray-800">Code Folders:</h2>
            <div>
                <ul class="directory">
                    <li class="folder">Folder 1
                      <ul>
                        <li class="file">File 1</li>
                        <li class="folder">Subfolder 1
                          <ul>
                            <li class="file">File 2</li>
                          </ul>
                        </li>
                      </ul>
                    </li>
                    <li class="file">File 3</li>
                  </ul>
            </div>
        </div>
    </div>
</div>
{:else}
<div class="container mx-auto mt-10">
    <div class="text-center text-red-500 mt-4">Card not found</div>
</div>
{/if}

<style>
    /* Reset some default styles */
body, ul, li {
  margin: 0;
  padding: 0;
  list-style: none;
}

/* Basic styling for folder and file items */
.folder::before {
  content: "📁"; /* Unicode folder icon */
  margin-right: 4px;
}

.file::before {
  content: "📄"; /* Unicode file icon */
  margin-right: 4px;
}

/* Add some indentation for nested items */
ul {
  padding-left: 20px;
}

/* Style folder and file items differently */
.folder {
  font-weight: bold;
}

/* Style folder items to be expandable/collapsible (not functional) */
.folder ul {
  display: none;
}

.folder:hover ul {
  display: block;
}

</style>