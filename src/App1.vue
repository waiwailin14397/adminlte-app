<template>
	<Header />
	<div class="wrapper">
	  <!-- <router-view /> -->
	  <Form1 />
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
  import Form1 from './views/Form1.vue';
  
  export default {
	components: {
	  Header,
	  Footer,
	  Form1
	},
	data() {
	  return {
		currentView: 'form1', // Set the default view
	  };
	},
	// App-level logic goes here
  }
  </script>
  
  <style>
  /* Add your custom styles here */
  </style>
  