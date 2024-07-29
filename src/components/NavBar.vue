<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    websiteName: {
      required: true,
      type: String
    },
    buttonFirst: {
      required: true,
      type: String
    },
    buttonSecond: {
      required: true,
      type: String
    }
  },
  methods: {
    Searcher() {
      const searchThing = this.$refs.search as HTMLInputElement
      alert('search is currently under development: ' + searchThing.value)
    }
  }
})
</script>

<template>
  <nav>
    <div class="left">
      <h2>{{ websiteName }}</h2>
      <div class="buttons">
        <a href="#">{{ buttonFirst }}</a>
        <a href="#">{{ buttonSecond }}</a>
      </div>
    </div>
    <div class="search">
      <input type="text" name="search" id="search" ref="search" />
      <button type="button" @click="Searcher()">search</button>
    </div>
  </nav>
</template>

<style>
/* Styles for the navigation bar */
nav {
  border: 3px solid whitesmoke;
  background-color: whitesmoke;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 20px; /* Added padding for better spacing */
}

/* Container for the website name and buttons */
.left {
  display: flex;
  align-items: center;
}

/* Container for the buttons */
.buttons {
  display: flex;
  gap: 20px; /* Space between buttons */
  margin-left: 20px; /* Space between website name and buttons */
}

/* Container for the search input and button */
.search {
  display: flex;
  align-items: center;
}

/* Styles for links */
a {
  border: 2px solid green;
  border-radius: 10px;
  padding: 10px;
  background-color: green;
  color: white;
  text-decoration: none;
  transition:
    background-color 0.5s ease,
    color 0.5s ease;
}

/* Hover effect for links */
a:hover {
  background-color: whitesmoke;
  color: black;
}
</style>
