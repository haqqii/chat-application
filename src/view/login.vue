<template>
  <div class="login-container">
    <div class="logo-container">
      <img src="../assets/logo.png" alt="Logo" class="logo" />
    </div>
    <div class="form-container">
      <div class="form-box">
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
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  padding: 20px;
  box-sizing: border-box; /* Include padding in the total width */
}

.logo-container {
  text-align: center;
  margin-bottom: 20px;
}

.logo {
  margin: auto;
  max-width: 100px;
}

.form-container {
  max-width: 350px; /* Set a maximum width for the form container */
  width: 100%; /* Take up the full width available */
}

.form-box {
  background-color: #fff;
  border: 1px solid #e1e1e1;
  padding: 20px;
  display: flex;
  border-radius: 8px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}
.form-input {
  padding: 5px;
  border: 1px solid #e1e1e1;
  display: flex;
  border-radius: 4px;
  margin-top: 5px; /* Add a margin to separate label and input */
  margin-bottom: 10px; /* Add a margin at the bottom of the input */
}

.form-group {
  display: flex;
  flex-direction: column;
  margin-bottom: 10px;
}

.form-label {
  font-weight: bold;
  font-size: 14px;
  margin-bottom: 5px;
}

/* Media query for smaller screens */
@media screen and (max-width: 600px) {
  .form-group {
    margin-bottom: 15px;
  }

  .form-label {
    font-size: 12px;
  }

  .form-input {
    padding: 8px; /* Reduce padding for smaller screens */
    font-size: 14px;
  }

  .form-button {
    padding: 10px;
    font-size: 14px;
  }
}
</style>
