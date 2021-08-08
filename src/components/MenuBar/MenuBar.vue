<template>
  <div class="menu-app">
    <div class="drag-app"></div>
    <div class="controls">
      <button class="minimize" @click="minimize">_</button>
      <button class="help">?</button>
      <button class="close" @click="close">✕</button>
    </div>
  </div>
</template>

<script>
import { ipcRenderer } from "electron";
const ipc = ipcRenderer
export default {
  methods: {
    minimize () {
      ipc.send('minimizeApp')
    },
    close () {
      ipc.send('closeApp')
    }
  }
}
</script>

<style src="./style.scss" lang="scss" scoped>
