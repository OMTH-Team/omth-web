<template>
  <main>
    <div id="index_container" class="flex h-screen z-100">
      <div class="m-auto">
        <div class="p-8">
          <!-- <img src="~/assets/text.svg" class="glitch w-220"> -->
          <h1 class="glitch text-5xl text-white" />
        </div>
      </div>
    </div>
  </main>
</template>

<script lang="ts">
export default {
  mounted () {
    this.textGlitch()
    this.indexAnimation()
  },
  methods: {
    indexAnimation () {
      this.$anime({
        targets: '#index_container',
        opacity: [0, 1],
        duration: 1000,
        delay: 1000,
        easing: 'easeOutQuint'
      })
    },
    textGlitch () {
      // eslint-disable-next-line no-undef
      const writer = GlitchedWriter.create('.glitch', {}, () => {})
      const phrases = ['Abandon the old dying world', 'Embrace the new existence', 'The place of the dream', 'The paradise', 'Hidden in the virtual world', 'Cαεlum β']
      writer.queueWrite(phrases, 1000, false)
    }
  }
}

</script>
