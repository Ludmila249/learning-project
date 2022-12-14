<template>
  <div>
    <div class="container-card">
      <card-product 
        v-for="card of cardsList"
        :key="card.id"
        :src="card.src"
        :comunity="card.comunity"
        :time="card.time"
        :age="card.age"
        :name="card.name"
        :price="card.price"
        :sale="card.sale"
        :discount="card.discount"
        :styleCardsCatalog="true"
      />
    </div>
    <pagination
      :numbers="getNumber"
      @clickOnNumber="handlerClick"
    />
  </div>
</template>
    
<script>
import CardProduct from '@/components/cardProduct.vue'
import Pagination from './ui/Pagination.vue'

	export default  {
		props: {
			cardsProduct: {
				type: Array,
				default: () => [],
			}
		},

    data() {
      return {
        page: 0,
        number: 0,
      }
    },
		
		components: {
			CardProduct,
			Pagination
		},

    computed: {
      cardsList() {
        const data = [[]];
        let count = 7;
        let countIndex = 0;
        const page = this.page || 0;
        
        this.cardsProduct.forEach((element, index) => {
          if(index <= count) {
            data[countIndex].push(element)
            if(index === count) {
              count = count + 7;
              countIndex = countIndex + 1;
              data.push([page])
            }
          }
        });

        this.number = data.length;

        return data[this.page || 0];
      },

      getNumber() {
        return this.number;
      }
    },

    methods: {
      handlerClick(index) {
        this.page = index - 1;
      }
    }
	}

</script>

<style lang="scss" scoped>
	.container-card {
		max-width: 825px;
		background:  #E5E5E5;
		display: flex;
		flex-wrap: wrap;
		margin-left: 30px;
		margin-bottom: 20px;
	}
</style>


