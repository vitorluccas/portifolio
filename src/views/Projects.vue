<script setup>
import HeaderComponent from '../components/HeaderComponent.vue';
import FooterComponent from '../components/FooterComponent.vue';
import { ref } from 'vue';

 const projects = ref([
        {
          id: 1,
          title: "EcoCharge",
          description:"Estações de recarga para veículos elétricos abastecidas com energia solar.",
          image: null,
        },
        {
          id: 2,
          title: "FinWise",
          description:"Aplicativo de gestão financeira pessoal com análise de gastos e projeções automáticas.",
          image: "finwise.png",
        },
        {
          id: 3,
          title: "SmartAgro",
          description:"Sistema de monitoramento agrícola com sensores IoT para otimizar irrigação e produtividade.",
          image: null,
        },
        {
          id: 4,
          title: "PicSphere",
          description:"Rede social para compartilhamento de fotos com filtros e álbuns colaborativos.",
          image: "picshere.png",
        },
        {
          id: 5,
          title: "HealthTrack",
          description:"Aplicativo para acompanhamento de saúde e hábitos, integrando dados de wearables",
          image: null,
        },
        {
          id: 6,
          title: "MentorHub",
          description:"Plataforma de conexão entre mentores e mentorados com videochamadas integradas.",
          image: "mentorhub.png",
        },
      ]);

</script>
<template>
  <HeaderComponent />
 <main>
      <section class="banner">
        <h1><span>Projects</span></h1>

        <p>
          Explore a selection of my work, showcasing how I approach design
          challenges. Each project reflects my commitment to creating
          user-centered experiences that blend functionality with aesthetic
          appeal.
        </p>
      </section>

      <section class="projects"> 
        <ul class="white-itens">
          <li v-for="projeto in projects">
            <h3>{{ projeto.title }}</h3>

            <p>{{ projeto.description }}</p>

            <p v-if="projeto.image != null">
              <img :src="'/images/'+ projeto.image" alt="">
            </p>
          </li>
        </ul>
      </section>
    </main>

  <FooterComponent />
</template>

<style>
section.projects{
    & ul li{
        & h3{
            font-weight: bold;
            font-size: 1.2rem;
            margin: 0.5rem;
        }
        & p{
            color: #757575;
            font-size: 0.9rem;
            line-height: 1.3rem;
            margin: 0.5rem;
        }

    }
}

</style>
