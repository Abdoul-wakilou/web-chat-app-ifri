<template>
<div class="row">
     <div class="col-6">
         
     </div>
     <div class="col-2">
         
     </div>
     <div class="col-3 section-container">
        <div class="close-button" @click="closeSection">
            <i class="bx bx-x-circle"></i>
        </div>
         <div class="container mt-3">
             <div class="upload">
                 <img src="img/photo.png" width = 125 height = 125 title = "photo de profil" @click="togglePopup">
                 <image-viewer v-if="showPopup" :image-src="imageUrl" @close-popup="togglePopup"/>
             </div>
             <div class="nom">
                 <span class="fs-2">Master IFRI</span>
             </div>
             <div class="username">
                 <span class="">@masterifri</span>
             </div>
             <div class="username">
                 <span class="text-success mr-2" style="font-size: 25px;"><i class="bx bxs-user-plus"></i></span>
                 <span class="text-danger" style="font-size: 25px;"><i class="bx bx-log-out"></i></span>
             </div>
         </div>
         <hr/>

         <div class="dropdown"  id="toggleIcon" data-toggle="collapse" data-target="#fileSection">
            <span>Fichiers récents (25 fichiers) <i class="bi bi-chevron-up ms-auto"></i></span>
        </div>
        <section class="collapse" id="fileSection">
            <div class="file">
                <ul>
                    <li><i class="bx bxs-file"></i> Content.pdf</li>
                    <li><i class="bx bxs-file"></i> Branding.pdf</li>
                    <li><i class="bx bxs-file"></i> Design changes.pdf</li>
                </ul>
            </div>
        </section>
        
        <div class="seemore">
                <a href="">Voir plus</a>
        </div>

          <hr/>

          <div class="dropdown" id="toggleIcon">
              Images (12 fichiers) <i class="bi bi-chevron-up ms-auto"></i>
          </div>
          <div class="mt-2" id="fileSection" style="text-align: center;">
                <div class="d-flex justify-content-center" id="imageContainer">
                    <div class="mr-3"><img src="img/photo.png" class="rounded mx-auto d-block" style="width: 70px; height: 70px;"></div>
                    <div class="mr-3"><img src="img/photo.png" class="rounded mx-auto d-block" style="width: 70px;  height: 70px;"></div>
                    <div class="mr-3"><img src="img/photo.png" class="rounded mx-auto d-block" style="width: 70px;  height: 70px;"></div>
                    <div class="mr-3"><img src="img/photo.png" class="rounded mx-auto d-block" style="width: 70px;  height: 70px;"></div>
                    <div class="mr-3"><img src="img/photo.png" class="rounded mx-auto d-block" style="width: 70px;  height: 70px;"></div>
                    <div class="mr-3"><img src="img/photo.png" class="rounded mx-auto d-block" style="width: 70px;  height: 70px;"></div>
                    <div><img src="img/photo.png" class="rounded mx-auto d-block" style="width: 70px; height: 70px;"></div>
                </div>
          </div>
          <div class="mt-4" style="text-align: center;">
            <button type="button" class="btn btn-outline-success rounded-pill" style="font-weight:bold;">Voir les membres</button>
          </div>
         </div>
         <div class="col-1">
         
        </div>
 </div>
  </template>
  
  <script>
  import ImageViewer from './ImageViewer.vue';

export default {
  name: 'GroupComponent',
  props: {
    msg: String
  },
  components: {
    ImageViewer
  },
  data() {
    return {
      showPopup: false,
      imageUrl: 'img/photo.png'
    };
  },
  methods: {
    togglePopup() {
      this.showPopup = !this.showPopup; 
    }
  }
}
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  
  </style>
  