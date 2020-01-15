<template>
  <div class="service-slider-wrapper">
    <vs-row>
      <vs-col vs-type="flex" vs-justify="center" vs-align="center" vs-w="10" vs-offset="1">
        <div class="service-slider">
          <div class="services-buttons">
            <vs-button class="service-button" v-bind:class="{active: sliderIndex === index ? true : false }" @click="currentService=service" type="flat" v-for="(service, index) in services" :key="`service-${index}`" :icon="service.buttonOptions.icon" >
              <span class="slider-btn-text">
                {{ service.buttonOptions.text }}
              </span>
            </vs-button>
          </div>
          <div class="service-content" v-if="currentService !== null">
            <div class="service-image" v-bind:style="{ backgroundImage: 'url('+ currentService.slider.image +')', backgroundSize: 'cover', backgroundRepeat: 'no-repeat' }"></div>
            <div class="service-details">
              <span class="service-title">{{currentService.slider.title}}</span>
              <span class="service-subtitle">{{currentService.slider.subTitle}}</span>
              <vs-button type="filled" class="btn-learn" color="rgb(60,176,101)">Learn More</vs-button>
            </div>
          </div>
        </div>
      </vs-col>
    </vs-row>
  </div>
</template>
<script>
export default {
  title: 'ServiceSlider',
  data () {
    return {
      sliderIndex: 0,
      services: [
        {
          buttonOptions: {
            icon: 'people', text: 'Liaison Services'
          },
          slider: {
            image: require('../assets/images/liaison-services.jpg'),
            title: 'Liaison Services',
            subTitle: 'Quality Representation on your behalf to your customers.',
            link: ''
          }
        },
        {
          buttonOptions: {
            icon: 'g_translate', text: 'Translations'
          },
          slider: {
            image: require('../assets/images/business-meeting.jpg'),
            title: 'Translations',
            subTitle: 'Human Grade Translation services.',
            link: ''
          }
        },
        {
          buttonOptions: {
            icon: 'assessment', text: 'Quality Management Systems'
          },
          slider: {
            image: require('../assets/images/quality-management.jpg'),
            title: 'Quality Management Systems',
            subTitle: 'ISO/TS16949 Consulting and Training. Custom made Traning. On site support.',
            link: ''
          }
        }
      ],
      currentService: null
    }
  },
  created () {
    this.currentService = {
      buttonOptions: {
        icon: 'people', text: 'Liaison Services'
      },
      slider: {
        image: require('../assets/images/liaison-services.jpg'),
        title: 'Liaison Services',
        subTitle: 'Quality Representation on your behalf to your customers.',
        link: ''
      }
    }
  },
  mounted: function () {
    this.slideChange()
  },
  methods: {
    slideChange () {
      setTimeout(() => {
        this.nextSlide()
        this.slideChange()
      }, 10000)
    },
    nextSlide () {
      this.sliderIndex++
      if (this.sliderIndex === 3) {
        this.sliderIndex = 0
      }
      this.currentService = this.services[this.sliderIndex]
    }
  }
}
</script>
<style scoped>
  @media (max-width: 700px) {
    .services-buttons {
      visibility: hidden;
    }
  }
</style>
<style scoped>
  @media (max-width: 800px) {
    .service-image {
      grid-column: span 2;
    }
    .service-details {
      grid-column: span 2;
    }
  }
</style>
<style scoped>
.service-slider-wrapper {
  height: 425px;
  display: block;
}
.service-slider-wrapper > .vs-row {
  max-width: 1200px;
  margin: 0 auto;
}
.service-slider {
  height: 400px;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr 5fr;
  width: 100%;
  margin-top: -1.5rem;
}
.services-buttons {
  width: auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0;
  grid-template-rows: 1fr;
  background-color: #fdfdfd;
}
.services-buttons > button.service-button {
  border: none;
  background: white;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: flex-start;
  padding: 1rem;
  color: #0F609F;
  font-weight: 600;
  letter-spacing: 1px;
  border-radius: 0 !important;
}
.services-buttons > button.service-button.active {
  border-bottom: 3px solid rgb(60, 176, 101) !important;
}
.service-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr;
  gap: 0;
}
.service-content > .service-image {
  height: inherit;
  width: inherit;
}
.service-content > .service-details {
  height: inherit;
  width: inherit;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 5%;
  background-color: #28395D;
  color: #e1e1e1;
  text-align: left;
  /*
  background: url('../assets/images/mexico-df.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  */
}
.service-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin: 0.25rem 0;
}
.service-subtitle {
  font-size: 1rem;
  font-weight: 500;
  margin: 1rem 0;
}
.btn-learn {
  border-radius: 0;
  color: #ffffff;
  width: 120px;
}
</style>
