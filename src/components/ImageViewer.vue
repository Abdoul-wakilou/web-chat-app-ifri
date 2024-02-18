<template>
    <div v-if="showPopup" class="image-viewer">
      <div class="popup-content">
        <img :src="imageSrc" alt="Image">
        <button @click="closePopup">Fermer</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      imageSrc: String // Propriété pour passer l'URL de l'image
    },
    data() {
      return {
        showPopup: false // État pour contrôler l'affichage du popup
      };
    },
    methods: {
      closePopup() {
        this.showPopup = false; // Méthode pour fermer le popup
      }
    }
  };
  </script>
  
  <style>
  /* Styles pour le popup */
  .image-viewer {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5); /* Fond semi-transparent */
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .popup-content {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
  }
  
  .popup-content img {
    max-width: 100%; /* Assurer que l'image ne dépasse pas la taille du popup */
  }
  
  .popup-content button {
    margin-top: 10px;
  }
  </style>
  