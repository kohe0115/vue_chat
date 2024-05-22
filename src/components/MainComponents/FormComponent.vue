<template>
  <div class="chat__form__contents">
    <input class="chat__form__content--input" name=""
      v-model="body"
    >
    <button class="chat__form__content--btn"
            @click="submit"
    >submit</button>
  </div>
</template>

<script>
export default {
  data: () => ({
    body: '',
  }),
  methods: {
    submit() {
      this.$emit('addData', this.body)
      this.body = '';
    }
  },
  props: ['messages']
}
</script>