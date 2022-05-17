<template>
  <div class="hello">
    <TwitterButton
      url="https://bizz-dome-uploads--demo.s3.amazonaws.com/media/2022/03/blob-45085_n-500x500.png"
      description="Descripción para el Tweet"
      :isBlank="false"
      btnText
    />
    <FacebookButton
      url="https://bizz-dome-uploads--demo.s3.amazonaws.com/media/2022/03/blob-45085_n-500x500.png"
      :isBlank="false"
      btnText
    />
    <LinkedInButton
      url="https://bizz-dome-uploads--demo.s3.amazonaws.com/media/2022/03/blob-45085_n-500x500.png"
      :isBlank="false"
      btnText
    />
  </div>
</template>

<script>
// Vue Share Component
import TwitterButton from "vue-share-buttons/src/components/TwitterButton.vue";
import FacebookButton from "vue-share-buttons/src/components/FacebookButton.vue";
import LinkedInButton from "vue-share-buttons/src/components/LinkedInButton.vue";

export default {
  name: "OneComponent",
  components: {
    TwitterButton,
    FacebookButton,
    LinkedInButton,
  },
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
