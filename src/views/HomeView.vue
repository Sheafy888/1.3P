<template>

  <section class="home-page">
    <div class="intro">
      <h1>Home Page</h1>
      <div>
      <p>Welcome to the home page of Tyler Sheaf portfolio. On here you will be able to find out about me,
        how to contact me and also to preview my projects and examples that I have completed. Click on the button above 
        to see my projects and examples of Vue.
      </p>
    </div>

    <button @click="showProjects"> View my projects</button>

    </div>
    <div class="project-list" v-if="projectsVisible">
    <h2>My projects</h2>
    <ul>
      <li>
        <h3>
          <a href="https://github.com/Sheafy888/SIT120" target="_blank"> 
          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRZ3e3_ugtLcVsfIV7EOK74Vl2Az19PuhH2VD7Vqts&s" height="80px">
          </a>
        </h3>
        <p>The project that is linked to the image is 1.1P where I display my skills in using html and css content. <br>
          Click the Image above to discover project</p>
      </li>
      <li>
        <h3>
          <a href="https://github.com/Sheafy888/Task-1.2" target="_blank"> 
          <img src="https://cdn-icons-png.flaticon.com/512/1087/1087815.png" height="80px">
          </a>
        </h3>
        <p>The project that is linked to the image is 1.2P where I show my skills in using responsive web design and Javascript. <br>
          Click the Image above to discover project</p>
      </li>
      <li>
        <h3>
          <a href="https://github.com/Sheafy888/1.3P" target="_blank">
          <img src="https://cdn-icons-png.flaticon.com/512/5956/5956592.png" height="80px">
          </a>
        </h3>
        <p>The project that is linked to the image is 1.3P where I show my skills with using HTML, CSS and Vue. Currently this website
          that you are on is the project. <br> This link will send you to the project with the work on it. </p>
      </li>
    </ul>

    <div class="project-vue">
    <h3> Alot of task was completed to learn about HTML, CSS and Javascript (Vue). Below here is an example of using vue on a website.</h3>
    <p>Type in the message box below: {{ message }}</p>
	<input v-model="message" placeholder="edit me" /><br><br>

  <div>Use the check box to select your name/names: {{ checkedNames }}</div>

  <input type="checkbox" id="harry" value="Harry" v-model="checkedNames" />
  <label for="harry"> Harry </label>
 
  <input type="checkbox" id="john" value="John" v-model="checkedNames" />
  <label for="john"> John </label>
 
  <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
  <label for="mike"> Mike </label>

  <input type="checkbox" id="n/a" value="Not Applicable" v-model="checkedNames" />
  <label for="n/a"> Not Applicable </label>

<br><br>
<span> Selected favourite car: {{ selected }}</span><br>
  <select v-model="selected">
    <option v-for="option in options" :value="option.value">
      {{ option.text }}
    </option>

    <!-- <option disabled value="">Please select one</option>
    <option>Audi</option>
    <option>BMW</option>
    <option>Chevrolet</option>
    <option>Ford</option>
    <option>Holden</option>
    <option>Toyota</option>
    <option>Subaru</option>
    <option>Volkswagon</option>
    <option>Other Car</option> -->
  </select> <br><br>

  <button @click="show = !show"> Click for Magic </button>
  <Transition name="slide-fade">
    <p v-if="show">Click on button to see what happens to me</p>
  </Transition>

  </div>

  </div>


  </section>
</template>

<script setup>
import { ref } from 'vue';
import mystyles from '../assets/mystyles.css'

const projectsVisible = ref(false);

const showProjects = () => {
  projectsVisible.value = true;
};


const message = ref('')
const message2 = ref('')
const checked = ref(true)
const checkedNames = ref([])
const picked = ref('One')
const selected = ref('')
const show = ref(true)

const options = ref([
  {text: 'Audi', value: 'Audi'},
  {text: 'Subaru', value: 'Subaru'},
  {text: 'Holden', value: 'Holden'},
  {text: 'Toyota', value: 'Toyota'},
  {text: 'Ford', value: 'Ford'},
  {text: 'BMW', value: 'BMW'}
])

</script>

<style>

.slide-fade-enter-active {
  transition: all 0.5s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.6s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}

</style>