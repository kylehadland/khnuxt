<template>
  <div>
    <h1>Resum&eacute; / CV</h1>
    <div style="margin: 20px 0" v-html="resume"></div>
    <h2>Work History</h2>
    <p>Please <nuxt-link to="contact">get in touch with me</nuxt-link> for a full CV with work history.</p>
  </div>
</template>

<script>
import resume from '../content/resume.md'

export default {
  computed: {
    resume() {
      return resume
    }
  }
};
</script>

<style>
h2 {
  color: var(--primary);
  font-size: 1.5rem;
}
ul{
  margin-bottom: 2rem;
}
</style>