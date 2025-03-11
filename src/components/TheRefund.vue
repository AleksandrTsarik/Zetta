<template>
  <div class="refund">
    <div class="refund__container">
      <div class="refund__inner">
        <div class="refund__block">
          <h2 class="title refund__title">Как оформить?</h2>
          <div class="refund-list">
            <ul>
              <li class="refund-list__item" v-for="(item, i) in list" :key="i">
                <div class="refund-list__title">{{ item.title }}</div>
                <div class="refund-list__text" v-html="item.text"></div>
                <div class="refund-list__memo" v-if="item.memo">
                  <svg
                    width="22"
                    height="20"
                    viewBox="0 0 22 20"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M21.6755 15.946L13.0539 1.6327C12.6229 0.908895 11.8616 0.474609 10.9994 0.474609C10.1373 0.474609 9.37599 0.908895 8.95409 1.6327L0.32331 15.946C-0.10777 16.6879 -0.10777 17.5656 0.32331 18.2984C0.75439 19.0313 1.52483 19.4746 2.37782 19.4746H19.6302C20.4924 19.4746 21.2628 19.0313 21.6847 18.2984C22.1066 17.5656 22.1066 16.6879 21.6755 15.946ZM20.098 17.3937C20.0521 17.4751 19.9145 17.656 19.6302 17.656H2.36865C2.08432 17.656 1.94674 17.466 1.90088 17.3937C1.85502 17.3213 1.7633 17.1041 1.90088 16.8598L10.5317 2.54651C10.6692 2.31128 10.9077 2.28413 10.9994 2.28413C11.0911 2.28413 11.3204 2.31128 11.4672 2.55556L20.0888 16.8689C20.2355 17.1041 20.1347 17.3213 20.0888 17.4027L20.098 17.3937ZM10.0822 6.80794H11.9166V12.2365H10.0822V6.80794ZM10.0822 14.046H11.9166V15.8556H10.0822V14.046Z"
                      fill="#FFBB00"
                    />
                  </svg>
                  {{ item.memo }}
                </div>
              </li>
            </ul>
          </div>
          <div class="refund__more">
            <a
              href="https://zettains.ru/calculators/osgop/?utm_source=2512541&utm_medium=9519741456&utm_campaign=9510823705"
              target="_blank"
              class="btn btn-dark"
              >Оформить полис онлайн</a
            >
          </div>
        </div>
        <div class="refund__block">
          <img src="../assets/img/peolpe.webp" alt="..." loading="lazy" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      list: [
        {
          title: 'Проверка разрешения на перевозку',
          text: 'Убедитесь, что у вас есть действующее разрешение. Проверьте его на сайте <a href="https://sicmt.ru/fgis-taksi" target="_blank">ФГИС «Такси».</a>',
        },
        {
          title: 'Оформление заявления',
          text: 'Укажите данные перевозчика, такси и пассажиров при оформлении заявления на сайте. Оформление занимает 5-7 минут',
        },
        {
          title: 'Оплата',
          text: 'После оформления заявления необходимо оплатить полис ОСГОП по появившейся ссылке, выбрав удобный вариант оплаты.',
          memo: 'Ссылка на оплату дейтсвует 20 минут. Если не успели оплатить, необходимо заново оформить заявления на получение полиса.',
        },
        {
          title: 'Получение полиса',
          text: 'После подтверждения и оплаты полис будет отправлен на указанный Вами Email в течение 2-4 часов.',
        },
      ],
    };
  },
};
</script>
<style lang="scss">
.refund {
  &__inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
    @media (max-width: 1023px) {
      grid-template-columns: 1fr;
    }
  }
  &__block {
    border-radius: var(--radius);
    background-color: var(--light);
    overflow: hidden;
    &:first-child {
      padding: 32px;
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  &__title {
  }
  &__more {
    margin: 0 auto;
    display: block;
    text-align: center;
  }
}
.refund-list {
  ul {
    list-style-type: none;
    counter-reset: num;
  }
  &__item {
    position: relative;
    margin: 0 0 20px;
    padding: 0 0 0 65px;
    //z-index: 1;
    &:before {
      content: counter(num);
      counter-increment: num;
      font-size: 20px;
      color: rgb(var(--primary));
      background-color: rgba(var(--primary), 0.1);
      width: 45px;
      height: 45px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 50%;
      position: absolute;
      left: 0;
      top: 0;
      z-index: 10;
      @media (max-width: 767px) {
        font-size: 18px;
      }
      @media (max-width: 575px) {
        font-size: 16px;
      }
    }
    &:after {
      content: '';
      position: absolute;
      display: block;
      border: dashed 1px rgb(var(--primary));
      height: calc(100% - 25px);
      left: 22px;
      top: 45px;
      z-index: 0;
    }
    &:last-child {
      &:after {
        display: none;
      }
    }
  }
  &__title {
    font-size: 20px;
    font-weight: 500;
    line-height: 110%;
    margin-bottom: 15px;
    @media (max-width: 767px) {
      font-size: 18px;
    }
    @media (max-width: 575px) {
      font-size: 16px;
      margin-bottom: 8px;
    }
  }
  &__text {
    font-size: 16px;
    font-weight: 400;
    @media (max-width: 575px) {
      font-size: 14px;
    }
    a {
      color: rgb(var(--primary));
    }
  }
  &__memo {
    background-color: rgba(255, 187, 0, 0.1);
    display: grid;
    grid-template-columns: 20px 1fr;
    gap: 15px;
    border-radius: 4px;
    padding: 15px;
    font-size: 16px;
    font-weight: 400;
    margin-top: 10px;
    @media (max-width: 575px) {
      font-size: 14px;
    }
  }
}
</style>
