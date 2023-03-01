<template>
  <div class="header">
    <div class="heading">
      <div class="heading__logo">
        <img src="@/assets/img/svg/logo.svg" alt="logo" />
      </div>
      <div class="heading__text">
        <span class="heading__text--main">Round Rock</span>
        <span class="heading__text--sec">Yard Maintenance</span>
      </div>
    </div>
    <div class="header__chips">Lorem Ipsum is simply dummy</div>
    <div class="header__text">
      <span>Lorem ipsum Lorem</span>
    </div>
    <div class="header__button">
      <a class="header__button--link" href="#">Help Me</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style lang="scss" scoped>
.header {
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-image: url(../assets/img/png/grass1.png);
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  padding: 52px 0;

  &__chips {
    margin-top: 50px;
    font-weight: $text-s;
    color: $text-color-main;
    padding: 20px 50px;
    font-size: 18px;
    line-height: 27px;
    background: rgba(0, 0, 0, 0.5);
    border-radius: 59px;
    text-align: center;
  }

  &__text {
    margin-top: 17px;
    max-width: 983px;
    color: $text-color-main;
    font-size: 64px;
    line-height: 66px;
    text-shadow: 0px 0px 40px rgba(0, 0, 0, 0.5);
    font-weight: $text-xxl;
    text-align: center;
  }

  &__button {
    margin: 100px 0 82px;

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

.heading {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 20px;

  &__logo {
    padding-top: 12px;
  }

  &__text {
    display: flex;
    flex-direction: column;
    text-align: center;
    color: $text-color-main;
    font-weight: $text-xl;

    &--main {
      font-size: 60px;
      line-height: 71px;
    }

    &--sec {
      font-size: 27px;
      line-height: 32px;
      letter-spacing: 0.26em;
    }
  }
}

@media screen and (min-width: 768px) {
  .heading {
    flex-direction: row;
  }
}

@media screen and (min-width: 1024px) {
  .header {
    &__text {
      font-size: 144px;
      line-height: 145px;
      min-width: 1000px;
    }
  }

  .heading {
    flex-direction: row;
  }
}
</style>