<template>
  <div class="insured-block-block">
    <div class="insured-block__container">
      <h2 class="title insured-block__title">Страховой случай. Что делать?</h2>
      <div class="insured-block__inner">
        <div class="insured-block__block" v-for="(item, i) in cards" :key="i">
          <div class="insured-block__img" v-html="item.ico"></div>
          <div class="insured-block__descr">
            <div class="insured-block__title">{{ item.title }}</div>
            <div class="insured-block__more">
              <a :href="item.url" class="btn btn-light" target="_blank"
                >{{ item.text }}
                <svg
                  width="20"
                  height="13"
                  viewBox="0 0 20 13"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M19.2704 4.57719L15.4487 0.474609L14.2703 1.73956L17.8221 5.55318L0 5.58002V7.3692L17.8721 7.34236L14.2695 11.2097L15.4478 12.4746L19.2704 8.37203C19.7377 7.86794 20 7.18574 20 6.47461C20 5.76348 19.7377 5.08128 19.2704 4.57719Z"
                    fill="#7D51FE"
                  />
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          ico: '<svg width="86" height="87" viewBox="0 0 86 87" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M38.7231 27.088L29.8468 18.2121L45.8112 16.4384L47.5851 0.474609L57.9234 10.8125L68.2618 0.474609L70.0356 16.4384L86 18.2121L76.7439 27.4679C74.2963 26.2352 71.5478 25.5579 68.681 25.5579H45.9868C43.4282 25.5579 40.9628 26.099 38.7231 27.088ZM86 64.9746V79.3079H78.833V86.4746H64.4991V79.3079H50.1652V86.4746H35.8312V79.3079H28.6643V64.9746C28.6643 62.5523 28.908 60.1622 29.3416 57.8079H85.3227C85.7563 60.1622 86 62.5523 86 64.9746ZM48.3734 68.5257C48.3734 65.5766 45.9832 63.1829 43.0305 63.1829H42.9624C40.0132 63.1829 37.6194 65.573 37.6194 68.5257V68.5938C37.6194 71.5429 40.0096 73.9365 42.9624 73.9365H43.0305C45.9797 73.9365 48.3734 71.5464 48.3734 68.5938V68.5257ZM77.0413 68.5257C77.0413 65.5766 74.6511 63.1829 71.6983 63.1829H71.6302C68.681 63.1829 66.2873 65.573 66.2873 68.5257V68.5938C66.2873 71.5429 68.6774 73.9365 71.6302 73.9365H71.6983C74.6475 73.9365 77.0413 71.5464 77.0413 68.5938V68.5257ZM45.9832 32.7246H68.6774C73.0314 32.7246 76.9266 35.3225 78.6037 39.343L82.9684 49.8135C83.083 50.0859 83.1583 50.3689 83.2658 50.6413H31.3985C31.506 50.3689 31.5848 50.0859 31.6959 49.8135L36.0606 39.3394C37.7341 35.3189 41.6293 32.7246 45.9832 32.7246ZM20.7806 58.2666L12.1874 60.0547L10.7289 53.0385L3.71249 54.4969L0.795533 40.4646C0.301013 38.0924 0.0537522 35.7024 0 33.3087L28.8219 27.3174L32.8211 31.3164C31.4236 32.8321 30.2733 34.6059 29.4491 36.5874L20.7842 58.2702L20.7806 58.2666ZM16.6811 46.309C19.5694 45.707 21.4256 42.8798 20.8236 39.9916L20.8093 39.9271C20.2073 37.0389 17.3799 35.1864 14.4916 35.7848L14.4271 35.7991C11.5388 36.4011 9.68257 39.2284 10.2846 42.1165L10.2989 42.181C10.901 45.0692 13.7283 46.9254 16.6166 46.3234L16.6811 46.309ZM22.2642 11.8409L39.318 9.94536L40.2497 1.57111C38.1677 0.571359 35.7739 0.248859 33.4052 0.739776L11.184 5.36586C6.93762 6.25094 3.63365 9.60136 2.81662 13.8619L0.673695 25.0025L1.38322 25.7013L22.7587 21.2579L19.9492 18.4486L22.2642 11.8409Z" fill="#7D51FE"/></svg>',
          title: 'Дорожно-транспортное происшествие',
          text: 'Подробнее',
          url: 'https://zettains.ru/strahovanie-fizicheskih-lic/avtostrahovanie/strahovoy-sluchay/',
        },
        {
          ico: '<svg width="86" height="87" viewBox="0 0 86 87" fill="none" xmlns="http://www.w3.org/2000/svg"><g clip-path="url(#clip0_439_633)"><path d="M86 27.7652L72.2902 36.1323L77.443 51.3436L57.3333 44.288V21.971H39.2483L34.9339 9.22507L48.6796 14.2131L53.6676 0.467407L62.0347 14.1772L77.2459 9.02441L72.2579 22.7701L86.0036 27.7581L86 27.7652ZM29.6449 40.8301C33.1351 37.322 33.1172 31.6496 29.6091 28.1594C26.101 24.6692 20.4286 24.6872 16.9384 28.1952C13.4483 31.7033 13.4662 37.3757 16.9743 40.8659C20.4823 44.3561 26.1548 44.3382 29.6449 40.8301ZM57.6308 73.3237L77.6938 79.1216L75.7015 86.0087L57.5913 80.7699L38.3381 86.1162C37.4888 86.3097 36.636 86.4029 35.8047 86.4029C31.4867 86.4029 27.5809 83.8874 25.8788 79.8526L14.9282 54.221H0V32.721H7.16667V47.0543H19.4718L43 43.9189V29.1377H50.1667V50.1933L36.6862 51.9886L44.2183 70.1919L56.1688 57.8043H75.25V64.971H59.2146L48.7871 75.7819L57.6308 73.3237Z" fill="#7D51FE"/></g><defs><clipPath id="clip0_439_633"><rect width="86" height="86" fill="white" transform="translate(0 0.474609)"/></clipPath></defs></svg>',
          title: 'Несчастный случай на дороге',
          text: 'Подробнее',
          url: 'https://zettains.ru/strahovanie-fizicheskih-lic/information/insuranced-accident/accident-approach/',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
.insured-block {
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
    padding: 24px;
    border-radius: var(--radius);
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 24px;
    @media (max-width: 575px) {
      grid-template-columns: 1fr;
      align-items: center;
      justify-content: center;
      text-align: center;
    }
    @media (max-width: 575px) {
      padding: 16px;
    }
    svg {
      path {
        fill: rgb(var(--primary));
      }
    }
  }
  &__img {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: rgba(var(--primary), 0.1);
    height: 135px;
    width: 135px;
    border-radius: 8px;
    @media (max-width: 575px) {
      margin: 0 auto;
      justify-content: center;
    }
  }
  &__descr {
    display: flex;
    flex-direction: column;
  }
  &__more {
    margin-top: auto;
    a {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      @media (max-width: 575px) {
        display: flex;
        justify-content: center;
      }
    }
  }
  &__title {
    font-size: 28px;
    font-weight: 600;
    margin-bottom: 24px;
    line-height: 1;
    @media (max-width: 767px) {
      font-size: 24px;
    }
    @media (max-width: 575px) {
      font-size: 20px;
    }
  }
}
</style>
