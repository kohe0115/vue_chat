<template>
  <div class="main__contents--content">
    <div class="chat__contents">
      <ChatContentComponent
          v-for="message in messages"
          :key="message.id"
          :content="message.content"
          :is-current="message.is_current"
      ></ChatContentComponent>
    </div>

    <FormComponent :messages="messages" @addData="addData"></FormComponent>
  </div>
</template>

<script>
import ChatContentComponent from "@/components/MainComponents/ChatContentComponent.vue";
import FormComponent from "@/components/MainComponents/FormComponent.vue";

export default {
  components: {ChatContentComponent, FormComponent},
  data() {
    return {
      messages: [
        {'id': 1, 'content': 'test1', 'is_current': (Math.floor(Math.random() * 10) + 1) % 2 === 0},
        {'id': 2, 'content': 'test2', 'is_current': (Math.floor(Math.random() * 10) + 1) % 2 === 0},
        {'id': 3, 'content': 'test3', 'is_current': (Math.floor(Math.random() * 10) + 1) % 2 === 0},
      ]
    }
  },
  methods: {
    addData(data) {
      this.messages.push(
          {
            'id': this.messages.slice(-1)[0].id + 1,
            'content': data,
            'is_current': true
          }
      );
    }
  }
}
</script>