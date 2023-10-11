<!-- <template>
    <div>
      <h1>User Details</h1>
      <form @submit.prevent="saveUserDetails">
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" v-model="user.name" id="name" />
        </div>
        <div class="form-group">
          <label for="birthdate">Birthdate:</label>
          <input type="date" v-model="user.birthdate" id="birthdate" />
        </div>
        <div class="form-group">
          <label for="age">Age:</label>
          <input type="number" v-model="user.age" id="age" />
        </div>
        <div class="form-group">
          <label for="email">Email:</label>
          <input type="email" v-model="user.email" id="email" />
        </div>
        <div class="form-group">
          <label for="description">Description:</label>
          <textarea v-model="user.description" id="description"></textarea>
        </div>
        <div class="form-group">
          <label for="profileImage">Profile Image URL:</label>
          <input type="text" v-model="user.profileImage" id="profileImage" />
        </div>
        <button type="submit">Save</button>
      </form>
  
      <div class="preview">
        <h2>Preview</h2>
        <p>Name: {{ user.name }}</p>
        <p>Birthdate: {{ user.birthdate }}</p>
        <p>Age: {{ user.age }}</p>
        <p>Birth Year: {{ calculatedBirthYear }}</p>
        <p>Email: {{ user.email }}</p>
        <p>Description: {{ user.description }}</p>
        <p>Profile Image: <img :src="user.profileImage" alt="Profile" /></p>
        <p>{{ votingEligibilityMessage }}</p>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, watch } from 'vue';
  
  const user = ref({
    name: '',
    birthdate: '',
    age: null,
    email: '',
    description: '',
    profileImage: ''
  });
  
  const calculatedBirthYear = ref(null);
  
  const saveUserDetails = () => {
    console.log('User details saved:', user.value);
  };
  
  const calculateBirthYear = () => {
    if (user.age) {
      const currentYear = new Date().getFullYear();
      calculatedBirthYear.value = currentYear - user.age;
    } else {
      calculatedBirthYear.value = null;
    }
  };
  
  watch(user, calculateBirthYear, { immediate: true });
  
  const getVotingEligibilityMessage = () => {
    return user.age >= 18 ? 'Eligible for voting' : 'Not eligible for voting';
  };
  
  const votingEligibilityMessage = ref(getVotingEligibilityMessage());
  
  watch(user, () => {
    votingEligibilityMessage.value = getVotingEligibilityMessage();
  });
  </script>
  
  <style scoped>
  /* Add your custom styles here */
  .user-details {
    max-width: 400px;
    margin: 0 auto;
  }
  
  .form-group {
    margin-bottom: 10px;
  }
  
  .preview {
    margin-top: 20px;
    border-top: 1px solid #ccc;
    padding-top: 10px;
  }
  </style>
   -->