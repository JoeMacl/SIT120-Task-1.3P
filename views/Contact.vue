<template>
  <div>
    <h1 class="h1">Contact me</h1>
    <form @submit.prevent="submitForm" class="contact-form">
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" required>
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      email: '', 
    };
  },
  methods: {
    submitForm() {
      console.log('Email submitted:', this.email);
    },
  },
};
</script>

<style scoped>

.contact-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh; 
}

.contact-form {
  text-align: center;
}

.form-group {
  margin-bottom: 20px;
}
.h1 {
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 600;
    font-size: 250%;
    text-align: center;
  }

</style>
