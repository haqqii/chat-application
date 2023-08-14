<template>
  <div class="flex items-center justify-center min-h-screen bg-gray-100">
    <div class="w-full max-w-md p-6 bg-white rounded-lg shadow-md">
      <h2 class="text-2xl font-semibold mb-4">Login</h2>
      <form @submit.prevent="login">
        <div class="mb-4">
          <label for="email" class="block mb-2 text-sm font-medium"
            >Email</label
          >
          <input
            v-model="email"
            type="email"
            id="email"
            class="
              w-full
              px-4
              py-2
              border
              rounded-md
              focus:outline-none focus:ring focus:border-blue-300
            "
            placeholder="Enter your email"
            required
          />
        </div>
        <div class="mb-4">
          <label for="password" class="block mb-2 text-sm font-medium"
            >Password</label
          >
          <input
            v-model="password"
            type="password"
            id="password"
            class="
              w-full
              px-4
              py-2
              border
              rounded-md
              focus:outline-none focus:ring focus:border-blue-300
            "
            placeholder="Enter your password"
            required
          />
        </div>
        <div class="mb-4">
          <button
            type="submit"
            class="
              w-full
              px-4
              py-2
              text-white
              bg-blue-500
              rounded-md
              hover:bg-blue-600
              focus:outline-none focus:ring
            "
          >
            Login
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: '',
      password: '',
    };
  },
  methods: {
    login() {
      // Implement your login logic here
      console.log('Login attempt:', this.email, this.password);
    },
  },
};
</script>

<style scoped>
/* Center the login form */
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
</style>
