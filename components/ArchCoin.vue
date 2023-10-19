<template>
  <img
    id="token"
    width="500"
    height="500"
    class="h-[300px] transform rotate-y-180 object-contain absolute top-0 right-0 mt-[80px] mr-[320px]"
    :src="imgSrc"
  />
</template>

<script>
export default {
  data() {
    return {
      imgId: "00000",
    };
  },
  computed: {
    imgSrc: function () {
      return (
        // "https://archway.io/assets/token-animation/ArchCoin_180_" +
        "/ArchCoin/ArchCoin_180_" + this.imgId + ".png"
      );
    },
  },
  beforeMount() {
    // preload all the imgs
    for (var i = 0; i < 40; i++) {
      var number = i.toString().padStart(5, "0");
      var img = new Image();
      img.src = "/ArchCoin/ArchCoin_180_" + number + ".png";
      console.log("loaded img n " + i);
    }
  },
  mounted() {
    var interval = 30;
    var totalImages = 40;

    setInterval(() => {
      var number = parseInt(this.imgId);

      if (number === totalImages - 1) {
        number = 0;
      } else {
        number++;
      }

      var newNumber = number.toString().padStart(5, "0");

      this.imgId = newNumber;
    }, interval);
  },
};
</script>
