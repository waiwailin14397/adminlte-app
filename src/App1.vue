<template>
	<Header />
	<div class="wrapper">
	  <!-- <router-view /> -->
	  <Home />
	</div>
	<Footer />
	<!-- ./wrapper -->
  </template>
  
  <script>
  import 'admin-lte/dist/css/adminlte.min.css';
  import 'admin-lte/dist/js/adminlte.min.js';
  import 'admin-lte/plugins/fontawesome-free/css/all.min.css';
  
  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import Home from './views/Home.vue';
  
  export default {
	components: {
	  Header,
	  Footer,
	  Home
	},
	data() {
	  return {
		currentView: 'home', // Set the default view
	  };
	},
	// App-level logic goes here
  }
  </script>
  
  <style>
  /* Add your custom styles here */
  </style>
  