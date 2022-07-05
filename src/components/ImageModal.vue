<template>
<div>
<!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" :data-bs-target="'#' + imgName + 'Modal'">
  View
</button>

<!-- Modal -->
<div class="modal fade" :id="imgName + 'Modal'" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">{{imgName}}</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <img :src="require(`@/assets/${image}`)" style="height: 90%;">
        <h1>{{artistName}}</h1>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
      </div>
    </div>
  </div>
</div>
</div>
</template>

<script>
export default {
  name: "ImgModal",
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