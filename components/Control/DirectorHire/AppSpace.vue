<template>
  <section class="space">
    <div class="container">
      <div class="space__inner">
        <h1 class="space__title">
          Подбор и найм <span>высококлассного</span> директора
        </h1>
        <div class="space__text">
          Проведем поиск, отбор кандидатов на руководящую должность и выберем подходящего!
        </div>
        <div class="space__btn">
          <a href="#!" class="space__link"> Нанять директора </a>
        </div>
        <div class="space__rocket">
          <img src="../../../assets/images/director-hire/direct.png" alt="director">
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent, onMounted } from 'vue'
import { insertBitrix4 } from '@/assets/js/bitrx-window'
export default defineComponent({
  setup () {
    // Вставка popup от Bitrix на кнопку
    onMounted(() => {
      try {
        insertBitrix4('.space__inner', '.space__btn')
      } catch (error) {}
    })
    return {}
  }
})
</script>

<style lang="scss" scoped>
@import '~/assets/scss/variables.scss';
.space {
  @include bgcenter('../../../assets/images/main-page/bg-rocket-earth.png');
}
.space__inner {
  padding: 196px 0 279px 0;
  position: relative;
}
.space__text {
  font-family: $ff2;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #B2B3B1;
  max-width: 540px;
}
.space__title {
  padding: 74px 0 25px 0;
  max-width: 620px;
  font-weight: 700;
  font-size: 45px;
  line-height: 55px;
  color: #FFFFFF;
  span {
    color: rgba(250, 255, 0, 1);
  }
}
.space__btn {
  margin-top: 50px;
}
.space__link {
  padding: 10px 40px;
  background: #F9FF05;
  box-shadow: 0px 0px 4px rgba(0, 0, 0, 0.15);
  border-radius: 50px;

  font-weight: 600;
  font-size: 18px;
  line-height: 33px;
  color: rgba(29, 29, 29, 0.9);
}
.space__rocket {
  position: absolute;
  bottom: 0;
  right: 0;
  max-width: 861px;
  max-height: 636px;
}

@media (max-width: 1024px) {
  .space__rocket {
    max-width: 790px;
    max-height: 512px;
    img {
      margin-left: 210px;
      width: 69%;
    }
  }
  .space__text{
    max-width: 450px;
  }
}
@media (max-width: 820px) {
  .space__rocket {
    max-width: 685px;
    max-height: 444px;
    img {
      margin-left: 300px;
      width: 60%;
    }
  }
}
@media (max-width: 768px) {
  .space {
    background-position: 40% 100%;
  }
  .space__rocket {
    img {
      margin-left: 312px;
      width: 53%;
    }
  }
}
@media (max-width: 480px) {
  .space {
    background-position: 30% 100%;
  }
  .space__rocket {
    img {
      margin-left: 0px;
      margin-top: 80px;
      width: 87%;
    }
  }
  .space__inner {
    padding-bottom: 295px;
  }
  .space__text {
    font-size: 18px;
    line-height: 22px;
  }
  .space__title {
    font-size: 36px;
    line-height: 45px;
  }
  .space__btn {
    margin-top: 40px;
  }
  .space__rocket {
    max-width: 438px;
    max-height: 284px;
  }
}
@media (max-width: 360px) {
  .space__text.one {
    font-size: 14px;
    line-height: 17px;
  }
  .space__title {
    font-size: 32px;
    line-height: 40px;
  }
  .space__link {
    font-size: 16px;
    padding: 10px 30px;
  }
  .space__rocket {
    max-height: fit-content;
    width: 100%;
  }
}
</style>
