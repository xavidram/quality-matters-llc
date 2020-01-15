<template>
  <div class='home'>
    <Jumbotron />
    <ServiceSlider id="servicesSection"/>
    <div class='parrallax-wrapper'>
      <div class='parrallax-content'>
        <vs-row vw-w='12'>
          <vs-col vs-type='flex' vs-justify='center' vs-align='center' vs-w='12'>
            <span class='title'>We can help you in your sorting and reworking needs!</span>
            <span
              class='subtitle'
            >Covering Mexico with partership offices in North-East of Mexico (Reynosa, Matamoros, Monterrey, Saltillo) and Central Mexico (queretaro, Toluca, Silao).</span>
          </vs-col>
        </vs-row>
      </div>
    </div>
    <ContactForm id="contactSection"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Jumbotron from '@/components/Jumbotron.vue'
import ServiceSlider from '@/components/ServiceSlider.vue'
import ContactForm from '@/components/ContactForm.vue'

export default {
  name: 'homepage',
  components: {
    Jumbotron,
    ServiceSlider,
    ContactForm
  }
}
</script>
<style scoped lang='scss'>
.home {
  display: flex;
  flex-direction: column;
  width: 100%;
  height: 100%;
  background: white;
}
.parrallax-wrapper {
  height: 300px;
  background: url('../assets/images/business-meeting-2.jpg');
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  display: block;
}
.parrallax-content {
  margin: 0 auto;
  height: inherit;
  width: inherit;
  background-color: #28395d;
  opacity: 0.85;
  color: #ffffff;
  display: block;
}
.parrallax-content > .vs-row {
  max-width: 1200px;
  margin: 0 auto;
  height: 100%;
}
.parrallax-content > .vs-row > .vs-col {
  flex-direction: column;
}
.vs-col > .title {
  font-size: 1.75rem;
  font-weight: 600;
}
.vs-col > .subtitle {
  font-size: 1rem;
  margin: 1rem 0;
  word-wrap: normal;
  letter-spacing: 1px;
  max-width: 80%;
}
</style>
