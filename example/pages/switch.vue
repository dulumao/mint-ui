<template>
  <div class="page-switch">
    <div class="page-title">Switch</div>
    <div class="page-part page-switch-padding">
      <mt-switch :value.sync="value1">
        <label v-text="value1"></label>
      </mt-switch>
    </div>

    <div class="page-part page-switch-padding">
      <mt-switch :value.sync="value4">
        <label v-text="value4"></label>
      </mt-switch>
    </div>

    <mt-cell :title="'选项 ' + value2">
      <mt-switch :value.sync="value2"></mt-switch>
    </mt-cell>
    <mt-cell :title="'选项 ' + value3">
      <mt-switch :value.sync="value3"></mt-switch>
    </mt-cell>
  </div>
</template>

<script>
export default {
  name: 'page-switch',

  data() {
    return {
      value1: false,
      value2: false,
      value3: true,
      value4: true
    };
  }
};
</script>

<style lang="css">
  @component-namespace page {
    @component switch {
      @descendent padding {
        padding: 0 10px;
      }
    }
  }
</style>
