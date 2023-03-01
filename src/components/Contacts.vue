<template>
  <div class="contacts">
    <div class="contacts__text">Contact Us</div>

    <div class="contacts__wrapper">
      <form class="contacts__wrapper--input" action="#">
        <input
          class="contact__input"
          type="text"
          name="name"
          id="name"
          placeholder=""
        />
        <input
          class="contact__input"
          type="email"
          name="email"
          id="email"
          placeholder=""
        />
        <input
          class="contact__input"
          type="tel"
          name="tel"
          id="tel"
          placeholder=""
        />
        <input class="contact__submit" type="submit" value="" />
      </form>

      <div class="contacts__wrapper--text">
        <div class="contact__text">
          <img
            class="e-mail__logo"
            src="@/assets/img/svg/mail.svg"
            alt="mail logo"
          />
          <p>test@gmail.com</p>
        </div>
        <div class="contact__text">
          <img class="" src="@/assets/img/svg/phone.svg" alt="phone logo" />
          <p>(303) 555-0105</p>
        </div>
        <div class="contact__text">
          <img
            class=""
            src="@/assets/img/svg/location.svg"
            alt="location logo"
          />
          <p>2715 Ash Dr. San Jose, South Dakota 83475</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.contacts {
  padding: 50px 0 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: #fcfcfc;

  &__text {
    font-size: 44px;
    line-height: 46px;
    font-weight: $text-xl;
    color: $text-color-second;
  }

  &__wrapper {
    display: flex;
    flex-direction: column;
    gap: 100px;

    &--input {
      margin-top: 70px;
      display: flex;
      flex-direction: column;
      gap: 14px;
      align-items: center;
    }

    &--text {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
  }
}

.contact__text {
  display: flex;
  justify-content: start;
  padding: 0 20% 0;
  gap: 20px;
}

.contact__input {
  background: #9fdea9;
  border: 1px solid transparent;
  height: 56px;
  padding: 20px;
  border-radius: 61px;
  min-width: 310px;
  outline: none;

  &:focus {
    border: 1px solid green;
  }

  &:invalid {
    border: 3px solid red;
  }
}

.contact__submit {
  border: 3px solid #4db96b;
  border-radius: 61px;
  background-color: #fcfcfc;
  width: 168px;
  height: 56px;
  color: #4db96b;
  font-size: 20px;

  &:hover {
    color: #fff;
    font-weight: $text-xl;
    background-color: #4db96b;
    transition: 1.5s;
  }
}

@media screen and (min-width: 768px) {
  .contacts__text {
    font-size: 64px;
    line-height: 96px;
  }
  .contact__input {
    min-width: 374px;
  }
}

@media screen and (min-width: 1024px) {
  .contacts__wrapper {
    flex-direction: row;
    align-items: center;
  }
}
</style>