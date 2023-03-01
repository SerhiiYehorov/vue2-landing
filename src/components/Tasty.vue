<template>
  <div class="testy">
    <div class="testy__title">
      <p class="testy__title--text">Testymonials</p>
    </div>

    <div class="testy__cards">
      <div class="testy__card">
        <div class="testy__card--photo">
          <img src="@/assets/img/svg/avatar.svg" alt="avatar" />
        </div>
        <div class="testy__card--article">
          <div class="card__article--header">Courtney Henry</div>
          <div class="card__article--text">
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. Lorem Ipsum has been the industry's standard dummy text
            ever since the 1500s, when an unknown printer took a galley of type
            and scrambled it to make a type specimen book
          </div>
          <div class="card__article--star">
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
          </div>
        </div>
      </div>

      <div class="testy__card">
        <div class="testy__card--photo">
          <img src="@/assets/img/svg/avatar.svg" alt="avatar" />
        </div>
        <div class="testy__card--article">
          <div class="card__article--header">Courtney Henry</div>
          <div class="card__article--text">
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. Lorem Ipsum has been the industry's standard dummy text
            ever since the 1500s, when an unknown printer took a galley of type
            and scrambled it to make a type specimen book
          </div>
          <div class="card__article--star">
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
          </div>
        </div>
      </div>

      <div class="testy__card">
        <div class="testy__card--photo">
          <img src="@/assets/img/svg/avatar.svg" alt="avatar" />
        </div>
        <div class="testy__card--article">
          <div class="card__article--header">Courtney Henry</div>
          <div class="card__article--text">
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. Lorem Ipsum has been the industry's standard dummy text
            ever since the 1500s, when an unknown printer took a galley of type
            and scrambled it to make a type specimen book
          </div>
          <div class="card__article--star">
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
          </div>
        </div>
      </div>

      <div class="testy__card">
        <div class="testy__card--photo">
          <img src="@/assets/img/svg/avatar.svg" alt="avatar" />
        </div>
        <div class="testy__card--article">
          <div class="card__article--header">Courtney Henry</div>
          <div class="card__article--text">
            Lorem Ipsum is simply dummy text of the printing and typesetting
            industry. Lorem Ipsum has been the industry's standard dummy text
            ever since the 1500s, when an unknown printer took a galley of type
            and scrambled it to make a type specimen book
          </div>
          <div class="card__article--star">
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
            <img src="@/assets/img/svg/star.svg" alt="star" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.testy {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 26px;

  &__title {
    &--text {
      font-size: 44px;
      line-height: 46px;
      font-weight: $text-xl;
      color: $text-color-second;
    }
  }

  &__cards {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 45px;
    margin-bottom: 50px;
  }

  &__card {
    display: flex;
    flex-direction: column;
    gap: 14px;
    padding: 30px;
    border: 1px solid #6cb981;
    border-radius: 40px;
    max-width: 300px;
    align-items: center;
    text-align: center;

    &--article {
      display: flex;
      flex-direction: column;
      gap: 13px;
    }
  }
}

.card__article {
  &--header {
    color: #6cb981;
    font-size: 18px;
    line-height: 22px;
    font-weight: $text-l;
  }

  &--text {
    font-size: 14px;
    line-height: 22px;
    color: #0d4c14;
    font-weight: $text-xs;
  }

  &--star {
    display: flex;
    gap: 7px;
    justify-content: center;
  }
}

@media screen and (min-width: 768px) {
  .testy__cards {
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
  }
  .testy__title--text {
    font-size: 64px;
    line-height: 96px;
  }
}

@media screen and (min-width: 1024px) {
  .testy {
    padding: 0 10px;

    &__cards {
      flex-direction: row;
      flex-wrap: wrap;
      max-width: 1200px;
      justify-content: center;
    }

    &__card {
      flex-direction: row;
      max-width: 465px;
      text-align: start;
      align-items: start;
    }
  }

  .card__article--star {
    justify-content: start;
  }
}

@media screen and (min-width: 1280px) {
  .testy {
    &__card {
      max-width: 577px;
    }
  }
}
</style>