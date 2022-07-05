<template>
    <div class="card mt-2" style="width: 90%;">
    <img :src="require(`@/assets/${image}`)" class="card-img-top" alt="Logo" style="height: 12rem;">
    <div class="card-body">
        <h5 class="card-title">{{imgName}}</h5>
        <p class="card-text">{{artistName}}</p>
        <ImageModal :imgSource="imgSource" :imgName="imgName" :artistName="artistName"/>
    </div>
    </div>
</template>

<script>
import ImageModal from '@/components/ImageModal.vue'
export default {
  name: "ImgPanel",
  components: {
    ImageModal,
  },
  props: {
    imgSource: String,
    imgName: String,
    artistName: String
  },
  data(){
  return{
    image: this.imgSource
  }
}
};

</script>