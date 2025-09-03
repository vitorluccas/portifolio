<script setup>
import HeaderComponent from '../components/HeaderComponent.vue';
import FooterComponent from '../components/FooterComponent.vue';
import { ref } from 'vue';

 const connect = ref([
        {
          id: 1,
          emogi: "fa-brands fa-instagram",
          description:"Instagram",
        },
        {
          id: 2,
          emogi: "fa-brands fa-behance",
          description:"Behance",
        },
        {
          id: 3,
          emogi: "fa-brands fa-dribbble",
          description:"Dribble",
        },
        {
          id: 4,
          emogi: "fa-brands fa-linkedin-in",
          description:"LinkedIn",
        },
      ]);

</script>
<template>
  <HeaderComponent />
 <main>
        <section class="banner">

            <h1><span>Connect</span></h1>

            <p>
                I’m always open to new opportunities and collaborations. Whether you’re looking to start a project or just want to chat, feel free to reach out.
            </p>
        </section>

        <section class="connect">
            <ul class="white-itens">
                <li v-for="conectar in connect">
                     <a href="#"><span :class="conectar.emogi"></span>{{ conectar.description }}</a>
                </li>
            </ul>
        </section>
    </main>

  <FooterComponent />
</template>

<style>
section.connect {
    & ul {
        & li {
            text-align: center;
            & span {
                font-weight:bold ;
                padding: 0 15px 0 0;
            }
        } 
    }
}
</style>
