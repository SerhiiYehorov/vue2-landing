<template>
  <div class="about">
    <div class="about__title">
      <p class="about__title--text">About Us</p>
      <img
        class="about__title--img"
        src="@/assets/img/svg/branch.svg"
        alt="green branch"
      />
    </div>

    <div class="about__main">
      <div class="about__main--articles">
        <div class="article">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap into electronic typesetting,
          remaining essentially unchanged. It was popularised in the 1960s with
          the release of Letraset sheets containing Lorem Ipsum passages, and
          more recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </div>
        <div class="article">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap into electronic typesetting,
          remaining essentially unchanged. It was popularised in the 1960s with
          the release of Letraset sheets containing Lorem Ipsum passages, and
          more recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </div>
        <div class="article">
          Lorem Ipsum is simply dummy text of the printing and typesetting
          industry. Lorem Ipsum has been the industry's standard dummy text ever
          since the 1500s, when an unknown printer took a galley of type and
          scrambled it to make a type specimen book. It has survived not only
          five centuries, but also the leap into electronic typesetting,
          remaining essentially unchanged. It was popularised in the 1960s with
          the release of Letraset sheets containing Lorem Ipsum passages, and
          more recently with desktop publishing software like Aldus PageMaker
          including versions of Lorem Ipsum.
        </div>
      </div>

      <div class="about__main--button">
        <a class="about__main--link" href="#">Help Me</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.about {
  margin-top: 92px;
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-bottom: 26px;

  &__title {
    position: relative;
    margin-bottom: 50px;

    &--text {
      font-size: 44px;
      line-height: 66px;
      font-weight: $text-xl;
      color: $text-color-second;
      margin-top: 8px;
    }

    &--img {
      width: 80px;
      position: absolute;
      top: 38px;
      right: -40px;
    }
  }

  &__main {
    background-image: url(../assets/img/png/grass2.png);
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    padding: 154px 0 78px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 50px;

    &--articles {
      margin-bottom: 28px;
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 60px;
    }

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

.article {
  font-size: 18px;
  line-height: 24px;
  text-align: center;
  color: $text-color-main;

  max-width: 300px;
}

@media screen and (min-width: 768px) {
  .about__main--articles {
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
  }
  .about__title--text {
    font-size: 64px;
    line-height: 96px;
  }
  .about__title--img {
    width: 109px;
    top: 50px;
    right: -60px;
  }
  .article {
    max-width: 280px;
  }
  .about {
    &__main {
      &--articles {
        flex-direction: row;
      }
    }
  }
}
</style>