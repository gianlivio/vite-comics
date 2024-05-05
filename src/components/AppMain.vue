<script>
export default {
    data() {
        return {
            sections: [
            {
              title: 'DC COMICS',
             items: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News']
            },
            {
              title: 'SHOP',
              items: ['Shop DC', 'Shop DC Collectibles']
             },
            {
              title: 'DC',
              items: ['Terms Of Use', 'Privacy policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
            },
            {
              title: 'SITES',
             items: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
            }   
             ]
        };
    }
}
</script>

<template>
    <section class="main-content">
    <div class="content-section" v-for="section in sections" :key="section.title">
      <ul>
        <h4>{{ section.title }}</h4>
        <li v-for="item in section.items" :key="item">{{ item }}</li>
      </ul>      
    </div>
    <div class="logo-container">
      <img src="../assets/img/dc-logo-bg.png" alt="DC Logo" />
    </div>
  </section>

</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
@use "../style/partials/mixin" as *;

.main-content {
    @include flex($justify-content: space-evenly);
    background-image: url('../assets/img/footer-bg.jpg');
    background-size: cover;
    background-position: center;
    color: white;

    .content-section {  
        margin-bottom: 2rem;

        h4 {
        margin-bottom: 1rem;
        font-size: 1.2rem;
      
         }

        ul {
         list-style: none;
         margin: 0;
        padding: 0;

        li {
        margin-bottom: 0.5rem;
         }
        }
    } 
}
</style>
