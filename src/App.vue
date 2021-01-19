<template>
  <div>
    <my-header v-if="headerIsVisible"></my-header>
    <section v-if="mainIsVisible">
      <div class="container" @click="animation">
        <div>
          <img alt="Alex logo" src="./assets/alex-animation.gif" id="alexLogo" />
        </div>
        <div class="menu">
          <ul>
            <li @click="showBio">Bio</li>
            <li @click="showWork">Work</li>
            <li @click="showContact">Contact</li>
          </ul>
        </div>
      </div>
    </section>
    <bio-page v-if="bioIsVisible"></bio-page>
    <work-page v-if="workIsVisible"></work-page>
    <contact-page v-if="contactIsVisible"></contact-page>
  </div>
</template>

<script>
import WorkPage from './components/WorkPage.vue';
import BioPage from './components/BioPage.vue';
import ContactPage from './components/ContactPage.vue';
import MyHeader from './components/MyHeader.vue';

export default {
  name: 'App',
  components: {
    BioPage,
    WorkPage,
    ContactPage,
    MyHeader,
  },
  data() {
    return {
      mainIsVisible: true,
      bioIsVisible: false,
      workIsVisible: false,
      contactIsVisible: false,
      headerIsVisible: false,
    };
  },
  methods: {
    showBio() {
      this.bioIsVisible = true;
      this.headerIsVisible = true;
      this.mainIsVisible = false;
    },
    showWork() {
      this.workIsVisible = true;
      this.headerIsVisible = true;
      this.mainIsVisible = false;
    },
    showContact() {
      this.contactIsVisible = true;
      this.headerIsVisible = true;
      this.mainIsVisible = false;
    },
  },
};
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
/* MAIN PAGE SECTION STYLES */
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  max-height: 100vh;
}
.menu {
  font-size: 3rem;
  line-height: 1.5em;
  position: absolute;
  bottom: 40%;
  left: 50%;
  text-align: left;
}
ul {
  list-style: none;
}
ul:hover {
  cursor: pointer;
}

/* General Styles*/
section {
  min-height: calc(100vh - 25px);
}
h2 {
  margin-top: 0;
}
</style>
