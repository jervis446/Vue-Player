<template>
  <div id="VuePlayer">
    <vue-plyr ref="plyr">
      <video preload="none" id="player" autoplay controls crossorigin></video>
    </vue-plyr>
  </div>
</template>

<script>
import VuePlyr from "vue-plyr";
import Hls from "hls.js";

export default {
  name: "VuePlayer",
  components: {
    VuePlyr
  },
  computed: {
    player() {
      return this.$refs.plyr.player;
    }
  },
  mounted() {
    if (Hls.isSupported()) {
      let hls = new Hls();
      console.log(hls);
      hls.loadSource("https://content.jwplatform.com/manifests/vM7nH0Kl.m3u8");
      hls.attachMedia(this.player.media);
      window.hls = hls;
    }
  }
};
</script>