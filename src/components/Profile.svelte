<!-- src/components/Profile.svelte -->
<script>
    export let user = {
      username: 'john_doe',
      fullName: 'John Doe',
      email: 'john.doe@example.com',
      phone: '123-456-7890',
      address: '123 Main St, City, Country',
      college: 'Example University',
      branch: 'Computer Science',
      year: '2023',
      semester: 'Spring',
      // Add other user data as needed
    };
  </script>
  
  <main class="bg-white p-4 flex">
    <!-- Left Side: User Image -->
    <div class="w-1/4">
      <!-- svelte-ignore a11y-img-redundant-alt -->
      <img src="user-profile.png" alt="User Image" class="rounded-full h-auto w-48" />
    </div>
  
    <!-- Right Side: User Information -->
    <div class="w-3/4 pl-4">
        <h1 class="text-3xl font-semibold text-blue-500 mb-2">{user.username}</h1>
        <p class="text-gray-700 text-lg mb-2"><strong>Full Name:</strong> {user.fullName}</p>
        <p class="text-gray-700 text-lg mb-2"><strong>Email:</strong> {user.email}</p>
        <p class="text-gray-700 text-lg mb-2"><strong>Phone:</strong> {user.phone}</p>
        <p class="text-gray-700 text-lg mb-2"><strong>Address:</strong> {user.address}</p>
        <p class="text-gray-700 text-lg mb-2"><strong>College/University:</strong> {user.college}</p>
        <p class="text-gray-700 text-lg mb-2"><strong>Branch:</strong> {user.branch}</p>
        <p class="text-gray-700 text-lg mb-2"><strong>Year:</strong> {user.year}</p>
        <p class="text-gray-700 text-lg mb-2"><strong>Semester:</strong> {user.semester}</p>
        <!-- Add other user information as needed -->
      </div>
  </main>
  