<template>
	<div class="pagination">
		<ul class="pagination__list">
			<li>
				<button class="pagination__arrows pagination__arrows--prev"></button>
			</li>
      <div class="pagination__wrap">
        <li v-for="item in itemNumbers" :key="item">
          <button 
            class="pagination__page"
            @click="handlerClick(item)" 
          >
            {{ item }}</button>
        </li>
      </div>

			<li>
				<button class="pagination__arrows pagination__arrows--next"></button>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
	props: {
		numbers: {
			type: Number,
			default: 1,
		}
	},
	
	data() {
		return {

		}
	},
	computed: {

		itemNumbers() {
			return this.numbers;
		}
	},
	methods: {
		handlerClick(index) {
			this.$emit("clickOnNumber", index);
		}
	}
  
}
</script>

<style lang="scss" scoped>
	.pagination {
		margin: 0 auto;
		height: 27px;
		width: 250px;

    &__wrap {
      display: flex;
    }

    &__list {
      display: flex;
      align-items: center;
    }
    

		&__page {
      width: 27px;
      height: 27px;
			border: 1px solid #2A2A2A;
			border-radius: 7px;
			margin: 0 10px;

      font-family: 'Trebuchet MS';
      font-weight: 700;
      font-size: 19px;
      line-height: 22px;
      color: #2A2A2A;
		}

    &__arrows {
      position: relative;
      width: 20px;
      height: 20px;
      background: inherit;

      &::before {
        content: "";
        position: absolute;
        width: 8px;
        height: 8px;
        top: 4px;
        left: 5px;
        border-left: solid 2px #2A2A2A;
        border-bottom: solid 2px #2A2A2A;
      }

      &--prev::before {
        transform: rotate(45deg);
      }

      &--next::before {
        transform: rotate(230deg);
      }
    }
	}
</style>