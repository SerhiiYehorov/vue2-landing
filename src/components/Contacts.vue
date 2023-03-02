<template>
  <div class="contacts">
    <div class="contacts__text">{{ mainTitle }}</div>

    <div class="contacts__wrapper">
      <div class="contacts__wrapper--input">
        <input
          v-for="(input, index) in inputs"
          class="contact__input"
          v-model="input.text"
          :key="index"
          :type="input.type"
          :name="input.name"
          :placeholder="input.placeholder"
        />
        <button class="contact__submit" @click="submit">Contact Me</button>
      </div>

      <div class="contacts__wrapper--text">
        <template v-for="contact in contacts">
          <a
            v-if="contact.type !== address"
            class="contact__text"
            :key="contact.type"
          >
            <img :src="contact.src" :alt="contact.alt" />
            <p>{{ contact.text }}</p>
          </a>
          <p v-else class="contact__text" :key="contact.type">
            <img :src="contact.src" :alt="contact.alt" />
            <span>{{ contact.text }}</span>
          </p>
        </template>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactUs",
  data() {
    return {
      mainTitle: "Contact Us",

      contacts: [
        {
          src: require("@/assets/img/svg/mail.svg"),
          alt: "mail logo",
          text: "test@gmail.com",
          type: "email",
        },

        {
          src: require("@/assets/img/svg/phone.svg"),
          alt: "phone logo",
          text: "(303) 555-0105",
          type: "phone",
        },
        {
          src: require("@/assets/img/svg/location.svg"),
          alt: "location logo",
          text: "2715 Ash Dr. San Jose, South Dakota 83475",
          type: "address",
        },
      ],

      inputs: [
        {
          class: "contact__input",
          type: "text",
          name: "name",
          id: "name",
          placeholder: "type your Name",
          text: "",
        },
        {
          class: "contact__input",
          type: "email",
          name: "email",
          id: "email",
          placeholder: "type your email",
          text: "",
        },

        {
          class: "contact__input",
          type: "tel",
          name: "tel",
          id: "tel",
          placeholder: "type your number",
          text: "",
        },
      ],
    };
  },

  methods: {
    submit() {
      const message = {
        name: this.inputs[0].text,
        email: this.inputs[1].text,
        tel: this.inputs[2].text,
      };
      console.log(message);
    },
  },
};
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
  cursor: pointer;
}

.contact__input {
  color: $text-color-third;
  background: #9fdea9;
  border: 1px solid transparent;
  height: 56px;
  padding: 20px;
  border-radius: 61px;
  min-width: 310px;
  outline: none;

  &::placeholder {
    color: $text-color-main;
  }
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

input:-webkit-autofill {
  -webkit-text-fill-color: $text-color-third;
  -webkit-box-shadow: 0 0 0px 1000px #9fdea9 inset;
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






