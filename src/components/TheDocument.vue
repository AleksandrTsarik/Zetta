<template>
  <div class="document" id="document">
    <div class="document__container">
      <div class="document__inner">
        <div class="document__block document-block">
          <h2 class="document-block__title title">Документы</h2>
          <div class="document-block__links">
            <div class="document-block__link" v-for="(item, i) in link" :key="i">
              <a :href="item.url" target="_blank">{{ item.name }}</a>
            </div>
          </div>
        </div>
        <div class="document__block">
          <img src="../assets/img/doc.png" alt="..." loading="lazy" />
          <img src="../assets/img/doc2.png" alt="..." loading="lazy" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      link: [
        {
          name: 'Правила страхования',
          url: 'https://zettains.ru/upload/rules/Правила%20ОСГОП%20на%20сайт.pdf',
        },
        {
          name: 'Осуществление Страховщиком страховой деятельности',
          url: 'https://zettains.ru/vss_info/#_ga=2.234079454.1387420564.1736426837-270621958.1735288439',
        },
        {
          name: 'Образец договора страхования',
          url: 'https://zettains.ru/local/modules/zetta.calc/lib/Pdf/osgop/files/obrazec_osgop.pdf',
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.document {
  &__inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
    @media (max-width: 1023px) {
      grid-template-columns: 1fr;
    }
  }
  &__block {
    background-color: var(--light);
    overflow: hidden;
    border-radius: var(--radius);
    &:first-child {
      padding: 32px;
      @media (max-width: 575px) {
        padding: 16px;
      }
    }
    img {
      width: 100%;
      height: 100%;
      &:first-child {
        @media (max-width: 767px) {
          display: none;
        }
      }
      &:last-child {
        display: none;
        @media (max-width: 767px) {
          display: block;
        }
      }
    }
  }
}
.document-block {
  &__links {
  }
  &__link {
    color: rgb(var(--primary));
    margin-bottom: 14px;
    border-bottom: solid 1px transparent;
    transition: 0.3s;
    display: inline-block;
    font-size: 16px;
    @media (max-width: 575px) {
      font-size: 14px;
    }
    &:hover {
      @media (min-width: 1023px) {
        border-color: rgb(var(--primary));
      }
    }
    &:last-child {
      margin-bottom: 0;
    }
  }
}
</style>
