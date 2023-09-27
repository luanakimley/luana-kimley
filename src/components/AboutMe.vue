<script setup lang="ts">
import NavBar from './NavBar.vue'

const skillCategories = ['Programming', 'Database', 'Design', 'Soft-Skills', 'Interests']

const skills = {
  programming: [
    'JavaScript',
    'React',
    'Node.js',
    'Express',
    'Three.js',
    'Vue.js',
    'TypeScript',
    'Angular',
    'RxJS',
    'Jasmine',
    'Python',
    'Flask',
    'Pygame',
    'NumPy',
    'Java',
    'JavaFX - FXML',
    'PHP',
    'Laravel',
    'C++',
    'Kotlin',
    'C#'
  ],
  database: ['MySQL', 'MongoDB', 'SQLite'],
  design: [
    'Figma',
    'Adobe Photoshop',
    'Adobe Illustrator',
    'Adobe InDesign',
    'Adobe After Effects'
  ],
  'soft skills': [
    'Teamwork',
    'Communication',
    'Problem Solving',
    'Time Management',
    'Collaboration',
    'Adaptability'
  ],
  interests: ['Gym', 'Travel', 'UI/UX Design', 'Full Stack Development', 'Culture Exchange']
}

const badgeClass = ['badge-pink', 'badge-blue', 'badge-yellow']

const getBadgeClass = (index: number) => badgeClass[index % badgeClass.length] + ' m-1'
</script>

<template>
  <NavBar />
  <div class="d-flex justify-content-center flex-column">
    <h1 class="fw-bold outline yellow text-uppercase mb-4 text-center pb-3 pt-5">About Me</h1>
    <div class="d-flex justify-content-center flex-column">
      <img
        src="../assets/profile/profile2.jpg"
        alt="Luana Kimley"
        class="rounded mx-auto mb-4"
        width="300"
      />
      <p class="my-2 mx-5 text-center">
        Hi there! My name is <strong class="blue">Luana Kimley,</strong> a final year Indonesian
        student studying<br />
        <strong class="pink">BSc in Computing in Software Development @ DkIT.</strong><br />
        Outside my studies, one thing I really love to do is to
        <strong class="yellow">travel</strong> and learning new
        <strong class="yellow">cultures!</strong>
      </p>
    </div>
    <div class="card-group m-5 mx-auto w-75">
      <div class="card">
        <div class="card-body">
          <h5 class="card-title mb-4 outline yellow text-center">Education</h5>

          <div class="card-text d-flex align-items-center">
            <div>
              <img src="../assets/flags/ireland.png" alt="Ireland" width="50" class="me-2" />
            </div>
            <div>
              <div class="blue">Dundalk Institute of Technology</div>
              <small>BSc, Computing in Software Development</small><br />
              <small>2020 - 2024</small>
            </div>
          </div>
          <div class="vertical-line-dashed"></div>
          <div class="card-text d-flex align-items-center">
            <div>
              <img src="../assets/flags/portugal.png" alt="Portugal" width="50" class="me-2" />
            </div>
            <div>
              <div class="blue">Instituto Superior Politécnico Gaya</div>
              <small>Erasmus+ Exchange, Computer Engineering</small><br />
              <small>Feb 2023 - Jul 2023 (Semester 6)</small>
            </div>
          </div>
          <div class="vertical-line"></div>
          <div class="card-text d-flex align-items-center">
            <div>
              <img src="../assets/flags/indonesia.png" alt="Indonesia" width="50" class="me-2" />
            </div>
            <div>
              <div class="blue">Saint Ursula Senior High School</div>
              <small>Natural Science and Mathematics</small><br />
              <small>2017 - 2020</small>
            </div>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="card-body">
          <h5 class="card-title mb-4 outline yellow text-center">Skills & Interests</h5>
          <div class="accordion accordion-flush" id="accordionExample">
            <div class="accordion-item" v-for="sc in skillCategories" :key="sc">
              <h2 class="accordion-header">
                <button
                  class="accordion-button blue"
                  type="button"
                  data-bs-toggle="collapse"
                  :data-bs-target="'#' + sc"
                  aria-expanded="false"
                  :aria-controls="sc"
                >
                  {{ sc.replace('-', ' ') }}
                </button>
              </h2>
              <div :id="sc" class="accordion-collapse collapse" data-bs-parent="#accordionExample">
                <div class="accordion-body">
                  <div class="d-flex flex-wrap">
                    <span
                      v-for="(item, index) in skills[sc.replace('-', ' ').toLowerCase()]"
                      :class="getBadgeClass(index)"
                      :key="item"
                    >
                      {{ item }}
                    </span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="card">
        <div class="card-body text-center">
          <h5 class="card-title outline yellow text-center">Contacts</h5>
          <div class="d-flex flex-column align-items-center justify-content-center h-75">
            <p class="card-text">
              <i class="bi-linkedin blue"></i
              ><a
                href="https://www.linkedin.com/in/luana-kimley/"
                target="_blank"
                class="p-2 link text-dark"
                >Luana Kimley</a
              >
            </p>
            <p class="card-text">
              <i class="bi-github"></i
              ><a href="https://github.com/luanakimley" target="_blank" class="p-2 link text-dark"
                >luanakimley</a
              >
            </p>
            <p class="card-text">
              <i class="bi-envelope-heart pink"></i
              ><a class="p-2 link text-dark">luanaa.kimley@gmail.com</a>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.accordion-button:not(.collapsed) {
  outline: none;
  box-shadow: none;
  background-color: white !important;
}

.link {
  cursor: pointer;
  text-decoration: none;
  position: relative;
  transition: all 0.7s;
  padding: 5px 5px;
  border: 3px solid transparent;
  &:hover {
    border-bottom: 3px solid #2671bc;
  }
}

.vertical-line {
  border-left: 1px solid #ccc; /* Adjust the color and width as needed */
  margin: 0 25px; /* Adjust the margin as needed for spacing */
  height: 30px; /* Adjust the height as needed */
}

.vertical-line-dashed {
  border-left: 1px dashed #ccc; /* Adjust the color and width as needed */
  margin: 0 25px; /* Adjust the margin as needed for spacing */
  height: 30px; /* Adjust the height as needed */
}
</style>
