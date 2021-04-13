<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div class="dashboard">
      <WidgetContentSmall slot="widget-content" :model="widgetContent" />
      <WidgetContentSmall slot="widget-content" :model="widgetContent" />
      <WidgetContentSmall slot="widget-content" :model="widgetContent" />
      <WidgetContentSmall slot="widget-content" :model="widgetContent" />
    </div>
  </div>
</template>

<script>
import WidgetContentSmall from './components/WidgetContentSmall.vue'

export default {
  name: 'App',
  components: {
    WidgetContentSmall
  },
  data: () => ({
    widgetContent: {
      primaryContent: "122 hours",
      primaryContentTitle: "Total hours billed this year",
      secondaryContent: "-5,3%",
      secondarySubContent: "10,4%"
    }
  })
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.dashboard {
  display: grid;
  grid-template-columns: auto auto auto auto;
  grid-template-rows: 140px 140px 140px 140px;
  gap: 10px;
}
</style>
