<script setup>
import NavBar from "@/components/NavBar.vue";
import Header from "@/components/Header.vue";
import Engagements from "@/components/Engagements.vue";
import Vehicles from "@/components/Vehicles.vue";
import Avis from "@/components/Avis.vue";
import AboutUs from "@/components/AboutUs.vue";
import Contact from "@/components/Contact.vue";
import Footer from "@/components/Footer.vue";
</script>

<template>
  	<main>
        <Header />
		<Engagements />
		<Vehicles />
		<Avis />
		<AboutUs />
		<Contact />
		<Footer />

        <NavBar />
  	</main>
</template>
