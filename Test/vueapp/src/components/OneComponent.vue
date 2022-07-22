<template>
<div>
    <div id="printMe">
        <QRCanvas :options="options" />
    </div>
    <button @click="print" class="no-print">Print</button>
    <!-- <TwitterButton
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
    /> -->
</div>
</template>

<script>
// Vue Share Component
// import TwitterButton from "vue-share-buttons/src/components/TwitterButton.vue";
// import FacebookButton from "vue-share-buttons/src/components/FacebookButton.vue";
// import LinkedInButton from "vue-share-buttons/src/components/LinkedInButton.vue";

import {
    QRCanvas
} from 'qrcanvas-vue'

export default {
    name: "OneComponent",
    components: {
        // TwitterButton,
        // FacebookButton,
        // LinkedInButton,
        QRCanvas
    },
    props: {},
    data() {
        return {
            output: null,
            globalOptions: {
              name: '_blank',
              specs: [
                'fullscreen=yes',
                'titlebar=yes',
                'scrollbars=yes'
              ],
              styles: [
                'https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css',
                'https://unpkg.com/kidlat-css/css/kidlat.css'
              ],
              timeout: 1000,
              autoClose: true,
              windowTitle: window.document.title, // whatever's the window title of the opener
            },
            localLandScapeOptions: {
              styles: [
                'https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css',
                'https://unpkg.com/kidlat-css/css/kidlat.css',
                'public/landscape.css', // must be the path of your public folder
              ]
            }
        }
    },
    computed: {
        options() {
            return {
                resize: true,
                data: 'http://localhost:8080/registry/kmjk/magic/1c1de2b3-3691-4aa5-8ac5-2858de96c9b8/2ad587a3-69ab-4025-8b7d-67e730e729b5',
                padding: 8,
                cellSize: 6
            }
        },
    },
    methods: {
      async print () {
        // Pass the element id here
        window.print()
        // await this.$htmlToPaper('printMe', this.globalOptions);
      }
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style>
@media print {
  body * {
    color: #fff;
    background: #000;
  }
  .no-print {
    display: none;
  }
}
</style>
