<template>
  <div>
    <div id="botui">
      <bot-ui></bot-ui>
    </div>
  </div>
</template>

<script>
// import vue from 'vue'
import BotUi from 'botui'

export default {
  data() {
    return {
      botui: ''
    }
  },
  components:{BotUi},
  mounted() {
    this.startBot
  },
  methods: {
    startBot() {
      this.botui = new BotUi('botui')
      this.botui.message.add({
        content: {
          text: 'Hello'
        }
      })
    }
  }
}
</script>