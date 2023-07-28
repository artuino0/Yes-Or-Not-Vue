<script>
export default {
  data() {
    return {
      inputValue: "",
      yesOrNotImage: null,
      yesOrNotAnswer: null,
      isLoading: false,
    };
  },
  methods: {
    fetchYesOrNot() {
      this.yesOrNotImage = null;
      this.yesOrNotAnswer = null;
      this.isLoading = true;

      fetch("https://yesno.wtf/api")
        .then((rs) => rs.json())
        .then((data) => {
          const { answer, image } = data;
          setTimeout(() => {
            this.yesOrNotImage = image;
            this.yesOrNotAnswer = answer;
            this.isLoading = false;
          }, 1500);
        });
    },
  },
  watch: {
    inputValue(value, oldValue) {
      if (!value.includes("?")) return;
      this.fetchYesOrNot();
    },
  },
};
</script>

<template>
  <div class="container">
    <div class="form">
      <h1>Yes or Not? or Maybe...</h1>
      <input
        type="text"
        name="question"
        id="question"
        placeholder="Ingresa tu pregunta..."
        v-model="inputValue"
      />

      <h2 v-if="yesOrNotAnswer" class="response-text">{{ yesOrNotAnswer }}</h2>
      <h2 v-if="isLoading">Si, no, tal vez?... Pensando</h2>
    </div>
    <div class="image-bg">
      <img
        :src="yesOrNotImage ? yesOrNotImage : 'https://placehold.co/600x400'"
        alt="response-image"
      />
    </div>
  </div>
</template>

<style scoped>
.form > h1 {
  font-size: 48px;
  margin: 0;
}

.form > input {
  width: 450px;
  margin: 3rem;
  padding: 0.7rem 1rem;
}
.container {
  text-align: center;
  width: 100vw;
  height: 100vh;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.response-text {
  text-transform: uppercase;
}

.image-bg {
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  position: fixed;
  z-index: -3;
}
.image-bg > img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.image-bg::before {
  content: "";
  position: fixed;
  z-index: 0;
  top: 0;
  left: 0;
  background: rgba(0, 0, 0, 0.7);
  width: 100vw;
  height: 100vh;
}
</style>
