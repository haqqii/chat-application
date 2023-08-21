<template>
  <div class="login-container">
    <div class="logo-container">
      <img src="path-to-your-logo.png" alt="Logo" class="logo" />
    </div>
    <div class="form-container">
      <div class="form-box">
        <h2 class="form-title">Login</h2>
        <form @submit.prevent="submitForm" class="form">
          <div class="form-group">
            <label for="email" class="form-label">Email</label>
            <input
              type="email"
              id="email"
              v-model="email"
              class="form-input"
              required
            />
          </div>
          <div class="form-group">
            <label for="password" class="form-label">Password</label>
            <input
              type="password"
              id="password"
              v-model="password"
              class="form-input"
              required
            />
          </div>
          <button type="submit" class="btn btn-primary form-button">
            Login
          </button>
        </form>
      </div>
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
    submitForm() {
      // Lakukan aksi login atau validasi di sini
      // Misalnya, Anda bisa mengirimkan data ke server atau melakukan validasi di sisi klien
      console.log('Email:', this.email);
      console.log('Password:', this.password);
    },
  },
};
</script>

<style scoped>
.login-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.logo-container {
  text-align: center;
  margin-bottom: 20px;
}

.logo {
  align-items: center;
  max-width: 100px;
}

.form-container {
  width: 300px;
}

.form-box {
  background-color: #fff;
  border: 1px solid #e1e1e1;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}

.form-title {
  font-size: 24px;
  margin-bottom: 20px;
}

.form {
  display: flex;
  flex-direction: column;
}

.form-group {
  margin-bottom: 15px;
}

.form-label {
  font-weight: bold;
  font-size: 14px;
  margin-bottom: 5px;
}

.form-input {
  padding: 10px;
  border: 1px solid #e1e1e1;
  border-radius: 4px;
  display: flex;
}

.form-button {
  padding: 10px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s;
}

.form-button:hover {
  background-color: #0056b3;
}
</style>
