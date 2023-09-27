<script setup lang="ts">
import NavBar from './NavBar.vue'
import kultura from '../assets/projects/kultura.png'
import kultura2 from '../assets/projects/kultura2.jpg'
import relievo from '../assets/projects/relievo.png'
import relievo2 from '../assets/projects/relievo2.jpg'
import wattwatch from '../assets/projects/wattwatch.png'
import wattwatch2 from '../assets/projects/wattwatch2.jpg'
import androidnews from '../assets/projects/androidnews.png'
import cityofextremism from '../assets/projects/cityofextremism.png'
import cityofextremism2 from '../assets/projects/cityofextremism2.jpg'
import ecommerce from '../assets/projects/ecommerce.gif'
import greenhouse from '../assets/projects/greenhouse.png'
import portometro from '../assets/projects/portometro.png'
import spacewarriors from '../assets/projects/spacewarriors.gif'
import studyabroad from '../assets/projects/studyabroad.png'
import studyabroad2 from '../assets/projects/studyabroad2.jpg'
import portfolio from '../assets/projects/portfolio.png'

const internationalProjects = [
  {
    title: 'Kultura',
    projectName: 'Start-IT',
    description:
      'Start-IT is an Erasmus+ funded project that aims to bring together students from several countries (Ireland, Poland, Belgium, Finland, Germany) to make an app on the topic of sustainable tourism. My team and I developed an app called Kultura, which aims to promote sustainable tourism in Porto, Portugal through folklores and legends around the city.',
    location: 'Porto, Portugal',
    link: 'https://www.figma.com/proto/Yw6z4byQI1RieqMmUhfzDU/Sisu?node-id=20-950&starting-point-node-id=20%3A950&mode=design&t=SS485cqkyDUZ8EvB-1',
    image: [kultura, kultura2],
    tags: [
      'Figma',
      'App Prototype',
      'UI/UX Design',
      'Teamwork',
      'Sustainable Tourism',
      'Public Speaking'
    ]
  },
  {
    title: 'Relievo',
    projectName: 'EIT Health I-Days',
    description:
      'Innovation Days (I-Days) promote health innovation among university students through 2-day programmes held in universities around Europe. My team and I developed a prototype to help manage chronic illness, specifically stress among people with hypertension. We came in 2nd overall out of 20 teams.',
    location: 'Dundalk, Ireland',
    link: 'https://www.figma.com/proto/I6NnC0YKRGbDpuGzqQHVmp/Relievo?type=design&node-id=2-35&t=0MtLYcDK4lvVArxw-0&scaling=scale-down&page-id=0%3A1&starting-point-node-id=2%3A35',
    image: [relievo, relievo2],
    tags: [
      'Figma',
      'App Prototype',
      'UI/UX Design',
      'Chronic Illness',
      'Teamwork',
      'Public Speaking'
    ]
  },
  {
    title: 'WattWatch',
    projectName: 'Towards 15-Minute Eco City',
    description:
      'Towards 15-Minute Eco City is an Erasmus+ funded project that brings students from Ireland, Portugal, France, and Poland to develop an app prototype that aims to promote sustainable 15-minutes eco cities. My team and I developed an app called WattWatch, which aims to promote sustainable energy consumption through smart houses',
    location: 'Lodz, Poland',
    link: 'https://www.figma.com/proto/F1XwzVHu7aVzy0OPjIEYOk/WattWatch?node-id=1-2&starting-point-node-id=1%3A2&mode=design&t=h2WMY0AFotYxekK3-1',
    image: [wattwatch, wattwatch2],
    tags: ['Figma', 'App Prototype', 'UI/UX Design', 'Smart House', 'Teamwork', 'Public Speaking']
  },
  {
    title: 'Study Abroad Blog',
    projectName: 'eCOAL',
    description:
      'eCOAL is an Erasmus+ funded app development coding project with students from Ireland, France, and Portugal. We developed a mobile newspaper application with a topic of our choice using React, Node.js, and SQLite. We chose the topic “Study Abroad” and also did presentations and pitches for our application.',
    location: 'Lens, France',
    link: 'https://github.com/quentinhnrt/study-abroad',
    image: [studyabroad, studyabroad2],
    tags: [
      'Responsive Web Design',
      'React',
      'SQLite',
      'Node.js',
      'Express',
      'Teamwork',
      'Public Speaking'
    ]
  },
  {
    title: 'City of Extremism',
    projectName: "JEU: Let's Play Together for the European Union",
    description:
      'Selected to be part of an EU-funded project, working with NGOs from France and the Netherlands, aiming to create games that can be used in secondary schools in Europe. My team consists of students from Ireland, Poland, Belgium, and Germany. We developed a demo of a game called City of Extremism using a Javascript game engine',
    location: 'Porto, Portugal',
    link: 'https://github.com/niall-oreilly21/CityOfExtremism',
    image: [cityofextremism, cityofextremism2],
    tags: ['Javascript', 'Game Development', 'Fighting Extremism', 'Teamwork', 'Public Speaking']
  }
]

const projects = [
  {
    title: "Luana's Portfolio",
    description:
      "A website to showcase my projects and skills, and to get to know more about me (which is what you're looking at now!). Hope you're enjoying what you see 😉 (it's still a work in progress!)",
    link: 'https://github.com/luanakimley/luana-kimley',
    image: portfolio,
    tags: ['HTML', 'CSS', 'Vue.js', 'Typescript', 'Bootstrap'],
    international: false
  },
  {
    title: 'Greenhouse Management System',
    description:
      'A system that will provide monitoring and control of a greenhouse that can be accessed through a website. My role was to develop the website using Flask and to design the UI/UX of the website using Figma.',
    link: 'https://github.com/luanakimley/GreenhouseManagementSystem',
    image: greenhouse,
    tags: [
      'Python',
      'Flask',
      'Figma',
      'MySQL',
      'Amazon Web Services',
      'PubNub',
      'HTML',
      'SCSS',
      'Javascript'
    ],
    international: false
  },
  {
    title: 'Porto Metro System',
    description:
      'A Java desktop application that will show several informations about the Porto Metro System, such as the schedule, journey planner, and stations. Also provides a feature that allows users to order metro cards. My role was to develop the GUI of the app using JavaFx with FXML and CSS.',
    link: 'https://github.com/niall-oreilly21/PortoMetro',
    image: portometro,
    tags: ['Java', 'JavaFx - FXML', 'MySQL', 'CSS', 'Apache Maven'],
    international: false
  },
  {
    title: 'Space Warriors',
    description:
      'A combat game developed in Python using Pygame. I worked mostly on the asset designs and also some of the game mechanics, such as the attack and potions.',
    link: 'https://github.com/niall-oreilly21/Space-Warriors',
    image: spacewarriors,
    tags: ['Python', 'Pygame', 'Game Development', 'Asset Design'],
    international: false
  },
  {
    title: 'E-Commerce Website',
    description:
      'A responsive web app that allows users to browse and buy products. Consists of three access levels, which are admin, logged-in user, and guest.',

    link: 'https://github.com/luanakimley/ecommerce-web-app',
    image: ecommerce,
    tags: ['React', 'Node.js', 'Express', 'HTML', 'MongoDB', 'SCSS', 'Javascript'],
    international: false
  },
  {
    title: 'Android News App',
    description:
      'An Android application that displays news from the News API. It is developed using Kotlin and Android Studio.',
    link: 'https://studentdkit-my.sharepoint.com/:v:/g/personal/d00234604_student_dkit_ie/ETCrY3KszYxDuKoFdmJr19YBSUne7HzrmQMoF6RXA1NV_g?e=YMLXKA&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZyIsInJlZmVycmFsQXBwUGxhdGZvcm0iOiJXZWIiLCJyZWZlcnJhbE1vZGUiOiJ2aWV3In19',
    image: androidnews,
    tags: ['Kotlin', 'Android Studio', 'Mobile Development'],
    international: false
  }
]

const badgeClass = ['badge-pink', 'badge-blue', 'badge-yellow']

const getBadgeClass = (index: number) => badgeClass[index % badgeClass.length] + ' m-1'
</script>

<template>
  <NavBar />
  <div class="d-flex justify-content-center flex-column">
    <h1 class="fw-bold outline yellow text-uppercase mb-4 text-center pb-3 pt-5">My Projects</h1>

    <span class="mx-auto my-4"
      ><a class="link" href="#international">International Projects</a> |
      <a class="link" href="#coding">Coding Projects</a></span
    >

    <hr class="w-75 m-4 mx-auto" />

    <h2 id="international" class="text-center p-4 pink"><strong>International Projects</strong></h2>
    <p class="text-center">Go to <a class="link" href="#coding">Coding Projects</a></p>
    <div class="container my-5 d-flex flex-wrap justify-content-center gap-5">
      <div
        v-for="project in internationalProjects"
        :key="project['title']"
        class="card"
        style="width: 20rem"
      >
        <div
          :id="project['title'].replace(/ /g, '-')"
          class="carousel slide"
          data-bs-ride="carousel"
        >
          <div class="carousel-inner">
            <div
              v-for="(img, index) in project['image']"
              :key="img"
              :class="{ 'carousel-item': true, active: index === 0 }"
            >
              <img :src="img" class="card-img-top" alt="Project picture" width="100%" />
            </div>
          </div>
          <button
            class="carousel-control-prev"
            type="button"
            :data-bs-target="'#' + project['title'].replace(/ /g, '-')"
            data-bs-slide="prev"
          >
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button
            class="carousel-control-next"
            type="button"
            :data-bs-target="'#' + project['title'].replace(/ /g, '-')"
            data-bs-slide="next"
          >
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
        <div class="card-body">
          <h3 class="card-title blue text-center m-3">
            <a class="nav-link" :href="project['link']" target="_blank"
              ><strong>{{ project['title'] }}</strong></a
            >
          </h3>
          <p class="card-text text-center">
            <strong class="yellow">{{ project['projectName'] }}</strong> |
            <span class="pink">{{ project['location'] }}</span>
          </p>
          <p class="card-text">
            {{ project['description'] }}
          </p>
          <div class="d-flex flex-wrap justify-content-center pt-3">
            <span
              v-for="(item, index) in project['tags']"
              :class="getBadgeClass(index)"
              :key="item"
            >
              {{ item }}
            </span>
          </div>
        </div>
      </div>
    </div>
    <hr class="w-75 m-4 mx-auto" />
    <h2 id="coding" class="text-center p-4 pink"><strong>Coding Projects</strong></h2>
    <p class="text-center">
      Go to <a class="link" href="#international">International Projects</a>
    </p>
    <div class="container my-5 d-flex flex-wrap justify-content-center gap-5">
      <div v-for="project in projects" :key="project['title']" class="card" style="width: 20rem">
        <img :src="project['image']" class="card-img-top" alt="Project picture" />
        <div class="card-body">
          <h3 class="card-title blue text-center m-3">
            <a class="nav-link" :href="project['link']" target="_blank"
              ><strong>{{ project['title'] }}</strong></a
            >
          </h3>
          <p class="card-text">
            {{ project['description'] }}
          </p>
          <div class="d-flex flex-wrap justify-content-center pt-3">
            <span
              v-for="(item, index) in project['tags']"
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
</template>

<style scoped>
.link {
  cursor: pointer;
  text-decoration: none;
  position: relative;
  transition: all 0.7s;
  padding: 5px 5px;
  border: 3px solid transparent;
  &:hover {
    border-bottom: 3px solid #f46a6a;
  }
}

.nav-link {
  cursor: pointer;
  position: relative;
  padding: 10px 20px;
  background: white;
  border-top-right-radius: 10px;
  border-bottom-left-radius: 10px;
  transition: all 1s;
  &:after,
  &:before {
    content: ' ';
    width: 10px;
    height: 10px;
    position: absolute;
    border: 0px solid #fff;
    transition: all 1s;
  }
  &:after {
    top: -1px;
    left: -1px;
    border-top: 3px solid #ffc612;
    border-left: 3px solid #f46a6a;
  }
  &:before {
    bottom: -1px;
    right: -1px;
    border-bottom: 3px solid #ffc612;
    border-right: 3px solid #f46a6a;
  }
  &:hover {
    border-top-right-radius: 0px;
    border-bottom-left-radius: 0px;
    &:before,
    &:after {
      width: 100%;
      height: 100%;
    }
  }
}

.carousel-control-prev-icon,
.carousel-control-next-icon {
  color: #00ff00 !important; /* Change to your desired button color */
}
</style>
