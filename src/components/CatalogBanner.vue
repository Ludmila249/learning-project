<template>
  <div class="banner">
    <div class="banner__container">
      <div class="banner__text-wrap">
        <p class="banner__name-event">Октябрьский турнир Warhammer 40000</p>
        <p class="banner__text">У тебя есть команда и вы готовы принять 
          участие в турнире Warhammer 40000?  
        </p>        
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
  .banner {
    position: relative;
    width: 100%;
    height: auto;
    background: $--color-main;

    min-height: 235px;
    background-image: url(@/assets/pictures/catalog_banner.jpg);
    background-repeat: no-repeat;
    background-position: 0 0;
    background-size: cover;
    

    &__img {
      position: absolute;
      width: 100%;
      min-height: 235px;

      object-fit: cover;
    }

    &__container {
      position: absolute;
      top: 0;
      left: 0;

      width: 100%;
      height: 100%;
      background: rgba(42, 42, 42, 0.45);
    }

    &__text-wrap {
      max-width: 1110px;
      margin: 0 auto;
      margin-top: 80px;
      padding-left: 20px;
      font-family: 'trebuchetms';
      font-weight: 400;
      font-size: 16px;
      line-height: 19px;

      color: $--color-white;
    }

    &__name-event {
      font-weight: 700;
      font-size: 22px;
      line-height: 26px;
      margin-bottom: 15px;
    }

    &__text {
      width: 370px;
    }

    @media (max-width: 768px) {
      display: none;
    }
  }

</style>