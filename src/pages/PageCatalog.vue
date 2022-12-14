<template>
  <Header />
  <main>
    <catalog-banner />
    <h2 class="catalog__title">Дуэльные настольные игры</h2>
    <div class="container">
      <Filter />
      <list-of-product 
        :cardsProduct="cardsProduct"
      />
    </div>
   

  </main>

  <Footer />
</template>

<script>
import Header from '@/components/layout/Header.vue'
import Footer from '@/components/layout/Footer.vue'
import CatalogBanner from '@/components/CatalogBanner.vue'
import Filter from '@/components/Filter.vue'
import ListOfProduct from '../components/ListOfProduct.vue'

  
export default {
  
  components: {
    Header,
    Footer,
    CatalogBanner,
    Filter,
    ListOfProduct,

  },
  
  data() {
    return {
      cardsProduct: [
         {
          id: 1,
          src: '/src/assets/images/chaos_space_marines.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: 'Magic: the Gathering',
          price: '3657',
        },
        {
          id: 2,
          src: '/src/assets/images/gravity_falls-card.jpg',
          comunity: '2-6',
          time: '20-40',
          age: '6',
          name: 'Гравити Фолз: Спасти Пухлю',
          price: '6000',
        },
        {
          id: 3,
          src: '/src/assets/images/broken_realms-card.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: "Broken Realms: Horrek's Dreadlance",
          price: '4999'
        },
        {
          id: 4,
          src: '/src/assets/images/star_wars-card.jpg',
          comunity: '3-8',
          time: '30-60',
          age: '16',
          name: 'Звездные войны Внешнее кольцо',
          price: '3957'
        },
         {
          id: 5,
          src: '/src/assets/images/chaos_space_marines.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: 'Magic: the Gathering',
          price: '3657',
        },
        {
          id: 6,
          src: '/src/assets/images/gravity_falls-card.jpg',
          comunity: '2-6',
          time: '20-40',
          age: '6',
          name: 'Гравити Фолз: Спасти Пухлю',
          price: '6000',
        },
        {
          id: 7,
          src: '/src/assets/images/broken_realms-card.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: "Broken Realms: Horrek's Dreadlance",
          price: '4999'
        },
        {
          id: 8,
          src: '/src/assets/images/star_wars-card.jpg',
          comunity: '3-8',
          time: '30-60',
          age: '16',
          name: 'Звездные войны Внешнее кольцо',
          price: '3957'
        },
         {
          id: 9,
          src: '/src/assets/images/chaos_space_marines.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: 'Magic: the Gathering',
          price: '3657',
        },
        {
          id: 10,
          src: '/src/assets/images/gravity_falls-card.jpg',
          comunity: '2-6',
          time: '20-40',
          age: '6',
          name: 'Гравити Фолз: Спасти Пухлю',
          price: '6000',
        },
        {
          id: 11,
          src: '/src/assets/images/broken_realms-card.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: "Broken Realms: Horrek's Dreadlance",
          price: '4999'
        },
        {
          id: 12,
          src: '/src/assets/images/star_wars-card.jpg',
          comunity: '3-8',
          time: '30-60',
          age: '16',
          name: 'Звездные войны Внешнее кольцо',
          price: '3957'
        },
         {
          id: 13,
          src: '/src/assets/images/chaos_space_marines.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: 'Magic: the Gathering',
          price: '3657',
        },
        {
          id: 14,
          src: '/src/assets/images/gravity_falls-card.jpg',
          comunity: '2-6',
          time: '20-40',
          age: '6',
          name: 'Гравити Фолз: Спасти Пухлю',
          price: '6000',
        },
        {
          id: 15,
          src: '/src/assets/images/broken_realms-card.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: "Broken Realms: Horrek's Dreadlance",
          price: '4999'
        },
        {
          id: 16,
          src: '/src/assets/images/star_wars-card.jpg',
          comunity: '3-8',
          time: '30-60',
          age: '16',
          name: 'Звездные войны Внешнее кольцо',
          price: '3957'
        },
        {
          id: 17,
          src: '/src/assets/images/broken_realms-card.jpg',
          comunity: '2-4',
          time: '30-60',
          age: '18',
          name: "Broken Realms: Horrek's Dreadlance",
          price: '4999'
        },
        {
          id: 18,
          src: '/src/assets/images/star_wars-card.jpg',
          comunity: '3-8',
          time: '30-60',
          age: '16',
          name: 'Звездные войны Внешнее кольцо',
          price: '3957'
        },
      ]

    }
  },
}

</script>

<style lang="scss" scoped>

  h1 {
    color: $--color-dove-gray;
    font-family: "trebuchetms";

  }

  .container {
    display: flex;  
    max-width: 1110px;
    margin: 0 auto;
    margin-top: 21px;
  }

  .catalog {
    &__title {
      max-width: 1110px;
      margin: 0 auto;
      margin-top: 20px;
    }
  }
    
  
</style>
