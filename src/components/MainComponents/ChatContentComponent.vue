<template>
  <div class="chat__content"
       :class="{'is__login__user' : isCurrent}"
       :style="{'flex-direction' : isCurrent ? 'row-reverse' : ''}"
  >
    <div class="chat__content--image"
         :class="{'is__login__user' : isCurrent}"
    >
      <img src="https://nekogazou.com/wp-content/uploads/2013/07/0142.jpg" class="avatar__image" alt="">
    </div>
    <div class="chat__content--message"
         :class="{'is__login__user' : isCurrent}"
    >
      <p>{{content}}</p>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
    }
  },
  props: ['content', 'isCurrent']
}

</script>