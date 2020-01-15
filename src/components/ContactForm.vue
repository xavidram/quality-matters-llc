<template>
    <div class="contact-wrapper">
        <div class="contact-content">
            <h2>GET IN TOUCH</h2>
            <div class="contact-details">
                <h5><vs-icon icon="phone"></vs-icon>+52 (81) 1609 6055</h5>
                <h5><vs-icon icon="email"></vs-icon><a href="mailto:contact@q-matters.com">contact@q-matters.com</a></h5>
            </div>
            <h4 style="margin: 2rem 0">Please feel free to get in touch anytime.</h4>
            <div class="form-container">
                <form class="contact-form">
                    <div class="form-group">
                        <vs-input label-placeholder="Your Name" v-model="name" />
                    </div>
                    <div class="form-group">
                        <vs-input label-placeholder="Your Email" v-model="email" />
                    </div>
                    <div class="form-group">
                        <vs-input label-placeholder="Your Phone" v-model="phone" />
                    </div>
                    <div class="form-group fg-textarea">
                        <vs-textarea label="Message" height="150px" v-model="message" counter="500" :counter-danger.sync="counterDanger" />
                    </div>
                    <vs-button type="filled" color="rgb(60,176,101)" class="btn-contact-send">Send</vs-button>
                </form>
            </div>
        </div>
    </div>
</template>
<script>
export default {
  title: 'ContactForm',
  data () {
    return {
      name: '',
      email: '',
      phone: '',
      message: '',
      counterDanger: false
    }
  }
}
</script>
<style scoped>
.contact-details {
    display: inline-flex;
    margin: 1rem 0;
}
.contact-details> h3 {
    margin-bottom: 1rem;
}
.contact-details > h5 {
    color: rgb(122,122,122);
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 1rem;
}
.contact-details > h5 > .vs-icon {
    margin-right: 0.5rem;
}
.form-container {
    max-width: 800px;
}
.form-group {
    width: 100%;
    margin: 0.25rem 0;
}
.form-group > div {
    width: 100%;
}
.fg-textarea {
    margin-top: 1rem;
}
.contact-form {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.btn-contact-send {
  border-radius: 0;
  color: #ffffff;
  width: 120px;
}
.contact-wrapper {
    display: block;
    padding: 0 1rem;
}
.contact-content  {
    max-width: 500px;
    margin: 5rem auto;
}
.input-span-placeholder {
    text-align: left;
}
.vs-con-textarea {
    border: 1px solid rgba(0,0,0,0.2) !important;
}
.fg-textarea > div > h4 {
    color: rgba(0,0,0,0.4) !important;
}
</style>
