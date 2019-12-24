<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>{{ msg }}</p>
    <p>{{ computedMsg }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class About extends Vue {
  data () {
    return {
      msg: 'msg of about'
    }
  }
  get computedMsg (): string {
    // @ts-ignore
    return `hi ${this.msg}`
  }
  created () {
    console.log('About created')
  }
}
</script>
