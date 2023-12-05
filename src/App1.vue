<template>
    <!-- <Header /> -->
    <h2><p v-if="message">{{ message }}</p></h2>
    <!-- <div class="wrapper">
        <Home />
    </div>
    <Footer /> -->
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
                message: "",
                error: ""
            };
        },
        mounted() {
            liff
            .init({
                liffId: import.meta.env.VITE_LIFF_ID
            })
            .then(() => {
                this.message = "LIFF init succeeded.";
            })
            .catch((e) => {
                this.message = "LIFF init failed.";
                this.error = `${e}`;
            });
        }
    }
</script>

<style>
/* Add your custom styles here */
</style>
