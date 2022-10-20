<script setup>
import Content from '../components/Content.vue'
import Nav from '../components/Nav.vue';
import Card from '../components/Card.vue';
import Footer from '../components/Footer.vue';
</script>

<template>
        <div id="navbar" class="container">
        <div class="row">
            <div class="col">
                <Nav id="Navbar" />
                <Content />
                <Card />
            </div>
        </div>
    </div>
    <footer>
    <Footer />
</footer>
</template>

<style>
#Navbar {
    -webkit-box-shadow: 5px 6px 14px 4px rgba(0,0,0,0.2); 
box-shadow: 5px 6px 14px 4px rgba(0,0,0,0.2);
border-radius: 10px;
margin-top: 30px;
}
body {
    background-color: lightgray;
}
</style>