<template>
  <textarea
    name=""
    id=""
    cols="30"
    rows="10"
    v-model="text"
    @keyup="toggleCase"
  ></textarea>
</template>
<script>
export default {
  data() {
    return {
      text: "",
      toggled: false,
    };
  },
  methods: {
    toggleCase(event) {
      if (event.key === "Escape" || event.key === "CapsLock") {
        this.text = this.toggled
          ? this.text.toLowerCase()
          : this.text.toUpperCase();
        this.toggled = !this.toggled;
      }
    },
  },
};
</script>

<style lang="sass" scoped></style>
