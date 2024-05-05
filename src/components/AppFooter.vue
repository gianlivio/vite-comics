<script>
export default {
  data() {
    return {
      icons: [
        { src: 'footer-facebook.png', alt: 'Facebook' },
        { src: 'footer-periscope.png', alt: 'Periscope'},
        { src: 'footer-pinterest.png', alt: 'Pinterest'},
        { src: 'footer-twitter.png', alt: 'Twitter'},
        { src: 'footer-youtube.png', alt: 'YouTube'}
      ]
    };
  }
}
</script>

<template>
    <footer class="footer-container">
      <div class="sign-up">
        <button>SIGN-UP NOW!</button>
      </div>
      <div class="social-media">
        <span>FOLLOW US</span>
        <ul class="social-icons">
          <li v-for="icon in icons" :key="icon.alt">
            <img :src="`../assets/img/${icon.src}`" :alt="icon.alt">
          </li>
        </ul>
      </div>
    </footer>
</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixin" as *;

.footer-container {
  @include flex(row, space-between, center);
  padding: 2rem;
  background-color: $dark-gray;
  color: white;

  .sign-up {
    button {
      padding: 0.8rem 1.6rem;
      background-color: transparent;  
      border: 2px solid $primary-color;  
      color: $primary-color;  
      font-size: 1rem;
      cursor: pointer;
      transition: background-color 0.3s, color 0.3s;

      &:hover {
        background-color: $primary-color;  
        color: white;  
      }
    }
  }

  .social-media {
    display: flex;
    align-items: center; 

    span {
      margin-right: 1rem; 
      font-weight: bold;
    }

    .social-icons {
      list-style: none;
      display: flex;
      margin-left: 1rem; 
      li {
        margin: 0 0.5rem;

        img {
          height: 30px;
        }
      }
    }
  }
}
</style>