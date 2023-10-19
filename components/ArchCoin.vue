<template>
  <div id="archCoin"></div>
</template>

<script>
export default {
  data() {
    return {
      imgId: 0,
      // array containing all the images urls
      imgSrcs: [...new Array(40).keys()].map(
        (i) =>
          "/ArchCoin/ArchCoin_180_" + i.toString().padStart(5, "0") + ".png"
      ),
    };
  },

  beforeMount() {
    var wrapper = document.getElementById("archCoin");

    this.imgSrcs.map((img, idx) => {
      // create a new image element
      var img = new Image();

      // add an id to the img element
      img.id = idx;

      // hide all the images except the first one
      if (idx > 0) {
        img.style.display = "none";
      }

      // set the src to the first img url
      img.src = this.imgSrcs[idx];

      // img should fill the wrapper
      img.width = 500;
      img.height = 500;
      img.classList.add(
        "h-[300px]",
        "transform",
        "rotate-y-180",
        "object-contain",
        "absolute",
        "top-0",
        "right-0",
        "mt-[80px]",
        "mr-[320px]"
      );

      // insert the img element inside the wrapper element
      wrapper.appendChild(img);
    });
  },

  mounted() {
    var interval = 33;
    var totalImages = 40;

    setInterval(() => {
      // get the current image
      var currentImage = document.getElementById(this.imgId);
      // hide the current image
      currentImage.style.display = "none";
      // increment the imgId if it's not the last image
      if (this.imgId < totalImages - 1) {
        this.imgId++;
      } else {
        // otherwise reset the imgId to 0
        this.imgId = 0;
      }

      // get the next image
      var nextImage = document.getElementById(this.imgId);
      // show the next image
      nextImage.style.display = "block";
    }, interval);
  },
};
</script>
