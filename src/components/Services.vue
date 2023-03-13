<template>
  <div class="services" id="services">
    <div class="services__title">
      <p class="services__title--text">{{ mainTitle }}</p>
      <img
        class="services__title--img"
        src="@/assets/img/svg/branch.svg"
        alt="green branch"
      />
    </div>

    <div class="services__cards">
      <div
        :class="[!isLight ? 'services__card--dark' : '', 'services__card']"
        v-for="(card, id) in cards"
        :key="id"
      >
        <img class="services__card--img" :src="card.src" :alt="card.alt" />
        <span class="services__card--title">
          {{ card.title }}
        </span>
        <span class="services__card--text">
          {{ card.text }}
        </span>
      </div>
    </div>
    <div class="services__button">
      <button
        class="services__button--link"
        @click.prevent="isLight = !isLight"
      >
        Change theme
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Services",

  data() {
    return {
      mainTitle: "Services",
      isLight: true,

      cards: [
        {
          src: require("@/assets/img/png/card1.png"),
          title: "Bom",
          text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled ",
          alt: "grass",
        },
        {
          src: require("@/assets/img/png/card2.png"),
          title: "Bum",
          text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled ",
          alt: "flowers",
        },
        {
          src: require("@/assets/img/png/card3.png"),
          title: "Bam",
          text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled ",
          alt: "lawn",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.services {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 50px;

  &__title {
    position: relative;

    &--text {
      font-size: 44px;
      line-height: 66px;
      font-weight: $text-xl;
      color: $text-color-second;
    }

    &--img {
      width: 80px;
      position: absolute;
      top: 35px;
    }
  }

  &__cards {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 22px;
  }

  &__button {
    margin-top: 28px;
    box-shadow: 0px 16px 30px rgba(50, 175, 100, 0.15);
    border-radius: 35px;

    &--link {
      padding: 22px 53px;
      background: radial-gradient(50% 50% at 50% 50%, #ffffff 0%, #f9f9f9 100%);
      border-radius: 35px;
      text-decoration: none;
      color: $link-color-main;
      font-size: 18px;
      line-height: 27px;
      font-weight: $text-l;
      box-shadow: 0px 16px 30px rgba(50, 175, 100, 0.15);
      border-color: transparent;

      &:hover {
        color: $text-color-main;
        background: radial-gradient(
          50% 50% at 50% 50%,
          #0cdd52 0%,
          #0d8b28 100%
        );
      }
    }
  }
}

.services__card {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 300px;
  box-shadow: 0px 10px 30px rgba(16, 51, 30, 0.1);
  border-radius: 30px;
  color: $text-color-third;

  &--dark {
    color: white;
    background-color: black;
  }

  &--img {
    width: 300px;
    margin-bottom: 30px;
  }
  &--title {
    font-size: 16px;
    line-height: 24px;
    font-weight: $text-xxl;
  }
  &--text {
    padding: 10px 30px 10px 30px;
    font-size: 14px;
    line-height: 20px;
    font-weight: $text-xs;
    margin-bottom: 10px;
  }
}

@media screen and (min-width: 768px) {
  .services__cards {
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
  }
  .services__title--text {
    font-size: 64px;
    line-height: 96px;
  }

  .services__title--img {
    width: 109px;
    top: 50px;
    left: 10px;
  }
}

@media screen and (min-width: 1024px) {
  .services {
    &__cards {
      flex-direction: row;
    }
  }
}
</style>