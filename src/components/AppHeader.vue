<script>
export default {
    data() {
        return {
            menuItems:[
                {
                    title:"CHARACTERS",
                    active:true,
                },
                {
                    title:"COMICS",
                    active:false,
                },
                {
                    title:"MOVIES",
                    active:false,
                },
                {
                    title:"TV",
                    active:false,
                },
                {
                    title:"GAMES",
                    active:false,
                },
 {
                    title:"COLLECTIBLES",
                    active:false,
                },
                {
                    title:"VIDEOS",
                    active:false,
                },
                {
                    title:"FANS",
                    active:false,
                },
                {
                    title:"NEWS",
                    active:false,
                },
                {
                    title:"SHOP",
                    active:false,
                },
            ]
        }
    }
}
</script> 

<template>
    <div class="header-container">
        <div class="header-logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
            <ul class="nav-list">
                 <li v-for="item in menuItems" :class="{ active:item.active }">
                <a href="">{{ item.title }}</a>
                </li>
            </ul>
    </div> 
    <div class="header-banner">
            <h3>--> content goes here <--</h3>
    </div>
    
  
   
</template>

<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;

    .header-container {
        @include flex(row, space-between, center);
        margin: 2em 10em;
        height: 80px;
        line-height: 80px;
       
    }

   .header-logo {
    text-align: center;
    padding-top: 20px;
    margin-right: 50px; 
   }

   ul {
    @include flex(row, center, center);
    list-style-type: none;
    gap: 1em;
    li {
   
        a {
            text-decoration: none;
              color: $text-color;
              padding-bottom: 60px;
              

              &:hover {
        color: $primary-color;
        }
    }

    &.active a {
            border-bottom: 4px solid $primary-color; // Sottolineatura blu
        }
   

    }
    
   }

   .header-banner {
    background-color: $dark-gray;


    h3 {
    color: $light-gray;
    margin-left: 6em;
    padding: 3em;
    }

   }  

</style>