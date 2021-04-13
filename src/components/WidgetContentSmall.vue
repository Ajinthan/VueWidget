<template>
  <div class="widget">
    <div class="widget-content-container">
      <div class="primary-widget-content">
        <span class="primary-content">{{ model.primaryContent }}</span>
        <span class="primary-content-title">{{ model.primaryContentTitle }}</span>
      </div>
      <div class="secondary-widget-content">
        <span>{{ model.secondaryContent }}</span>
        <span>{{ model.secondarySubContent }}</span>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'WidgetContentSmall',
  props: {
    model: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@mixin widget-content-default {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
}

.widget {
  display: flex;
  border: 2px solid #ddd;
}
.widget-content-container {
  display: grid;
  grid-template-columns: 70% 30%;
  grid-row: auto;
  width: 100%;
  padding: 15px;


  .primary-widget-content {
    @include widget-content-default();

    > .primary-content {
      font-size: 1.8em;
      font-weight: bold;
    }

    > .primary-content-title {
      font-size: 1.0em;
    }
  }

  .secondary-widget-content {
    @include widget-content-default();
  }
}
</style>
