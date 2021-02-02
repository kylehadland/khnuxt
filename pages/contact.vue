<template>
  <div class="container">
    <h1>Contact Me</h1>

    <b-form @submit.prevent="sendEmail" @reset="onReset">
      <b-form-group
        id="input-group-1"
        label="Email address:"
        label-for="input-1"
        description="We'll never share your email with anyone else."
      >
        <b-form-input
          id="input-1"
          v-model="email"
          type="email"
          placeholder="Enter email"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Your Name:" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="name"
          placeholder="Enter name"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-2"
        label="Phone Number: (optional)"
        label-for="input-3"
      >
        <b-form-input
          id="input-3"
          v-model="phone"
          placeholder="Enter phone number"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Message:" label-for="input-4">
        <b-form-textarea
          id="input-4"
          v-model="message"
          placeholder="Enter message"
          required
          rows="4"
        ></b-form-textarea>
      </b-form-group>
      <b-button type="submit" variant="primary">Submit</b-button>
      <b-button type="reset">Reset</b-button>
    </b-form>
  </div>
</template>

<script>
import emailjs from 'emailjs-com';

export default {
  data() {
    return {
      name: "",
      email: "",
      phone: "",
      message: ""
    }
  },
  methods: {
    sendEmail(e) {
      emailjs.send('service_lyohexo', 'template_tawnqea',  
        {
          name: this.name,
          email: this.email,
          phone: this.phone,
          message: this.message
        },'user_MZm1go1bySbviiFclxVt5')
        .then((result) => { 
          console.log('SUCCESS!', result.status, result.text) 
          this.onSuccess()
          this.onReset()
        }, (error) => { 
          this.onError(error)
          console.log('FAILED...', error)
        }
      )
    },
    onReset() {
      this.name = ''
      this.email = ''
      this.phone = ''
      this.message = ''
    },
    onSuccess() {
      this.$bvToast.toast('Message successfully sent. Thankyou.', {toaster: 'b-toaster-top-center', title: 'Success', autoHideDelay:3000, variant: 'success'})
    },
    onError(e) {
      this.$bvToast.toast('Message send failed. Error: ' + e, {toaster: 'b-toaster-top-center', title: 'Error', autoHideDelay:3000, variant: 'danger'})
    }
  }
}
</script>

<style>
</style>