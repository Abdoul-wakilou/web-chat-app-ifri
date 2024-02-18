<template>
  <div class="row">
     <div class="col-6">
         
     </div>
     <div class="col-2">
         
     </div>
     <div class="col-3 mr- section-container">
        <div class="close-button" @click="closeSection">
            <i class="bx bx-x-circle"></i>
        </div>
         <div class="container mt-3">
             <div class="upload">
                 <img src="img/photo.png" width = 125 height = 125 title = "photo de profil"> 
             </div>
             <div class="nom">
                 <span class="fs-2">Khaled</span>
             </div>
             <div class="username">
                 <span class="">@khaled45</span>
             </div>
         </div>

         <hr/>

         <div class="dropdown">
            <span id="toggleIcon">Fichiers récents (25 fichiers) <i class="bi bi-chevron-up ms-auto"></i></span>
        </div>

        <div class="file" id="fileSection">
            <ul>
                <li><i class="bx bxs-file"></i> Content.pdf</li>
                <li><i class="bx bxs-file"></i> Branding.pdf</li>
                <li><i class="bx bxs-file"></i> Design changes.pdf</li>
            </ul>
        </div>
        <div class="seemore">
                <a href="">Voir plus</a>
        </div>

          <hr/>

          <div class="dropdown" id="toggleIcon">
              <span style="font-weight: bold;">Images</span> (12 fichiers) <i class="bi bi-chevron-up ms-auto"></i>
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
            <button type="button" class="btn btn-outline-danger" style="font-weight: bold;">Block Khaled</button>
          </div>
          
         </div>
         <div class="col-1">
         
        </div>
 </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
