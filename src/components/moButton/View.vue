<template>
  <div>
    <div class="flex j-around btn-box">
      <mo-button>
        <template #title>默认按钮</template>
      </mo-button>
      <mo-button type="primary">
        <template v-slot:title>主要按钮</template>
      </mo-button>
      <mo-button type="success">
        <template v-slot:title>成功按钮</template>
      </mo-button>
      <mo-button type="info">
        <template v-slot:title>信息按钮</template>
      </mo-button>
      <mo-button type="warning">
        <template v-slot:title>警告按钮</template>
      </mo-button>
      <mo-button type="danger">
        <template v-slot:title>危险按钮</template>
      </mo-button>
    </div>
    <div class="flex j-around btn-plain">
      <mo-button plain>
        <template #title>朴素按钮</template>
      </mo-button>
      <mo-button type="primary" plain>
        <template v-slot:title>主要按钮</template>
      </mo-button>
      <mo-button type="success" plain>
        <template v-slot:title>成功按钮</template>
      </mo-button>
      <mo-button type="info" plain>
        <template v-slot:title>信息按钮</template>
      </mo-button>
      <mo-button type="warning" plain>
        <template v-slot:title>警告按钮</template>
      </mo-button>
      <mo-button type="danger" plain>
        <template v-slot:title>危险按钮</template>
      </mo-button>
    </div>
    <div class="flex j-around btn-round">
      <mo-button round>
        <template #title>圆角按钮</template>
      </mo-button>
      <mo-button type="primary" round>
        <template v-slot:title>主要按钮</template>
      </mo-button>
      <mo-button type="success" round>
        <template v-slot:title>成功按钮</template>
      </mo-button>
      <mo-button type="info" round>
        <template v-slot:title>信息按钮</template>
      </mo-button>
      <mo-button type="warning" round>
        <template v-slot:title>警告按钮</template>
      </mo-button>
      <mo-button type="danger" round>
        <template v-slot:title>危险按钮</template>
      </mo-button>
    </div>
    <div class="flex j-around btn-icon">
      <mo-button icon="search" circle></mo-button>
      <mo-button type="primary" icon="edit" circle></mo-button>
      <mo-button type="success" icon="check" circle></mo-button>
      <mo-button type="info" icon="message" circle></mo-button>
      <mo-button type="warning" icon="star-off" circle></mo-button>
      <mo-button type="danger" icon="delete" circle></mo-button>
      <!-- <i class="iconfont icon-check"></i> -->
    </div>
    <div class="flex j-around btn-disabled">
      <mo-button disabled>
        <template #title>默认按钮</template>
      </mo-button>
      <mo-button type="primary" disabled>
        <template v-slot:title>主要按钮</template>
      </mo-button>
      <mo-button type="success" disabled>
        <template v-slot:title>成功按钮</template>
      </mo-button>
      <mo-button type="info" disabled>
        <template v-slot:title>信息按钮</template>
      </mo-button>
      <mo-button type="warning" disabled>
        <template v-slot:title>警告按钮</template>
      </mo-button>
      <mo-button type="danger" disabled>
        <template v-slot:title>危险按钮</template>
      </mo-button>
    </div>
    <div class="flex j-around btn-disabled">
      <mo-button plain disabled>
        <template #title>朴素按钮</template>
      </mo-button>
      <mo-button type="primary" plain disabled>
        <template v-slot:title>主要按钮</template>
      </mo-button>
      <mo-button type="success" plain disabled>
        <template v-slot:title>成功按钮</template>
      </mo-button>
      <mo-button type="info" plain disabled>
        <template v-slot:title>信息按钮</template>
      </mo-button>
      <mo-button type="warning" plain disabled>
        <template v-slot:title>警告按钮</template>
      </mo-button>
      <mo-button type="danger" plain disabled>
        <template v-slot:title>危险按钮</template>
      </mo-button>
    </div>
    <div class="flex j-around">
      <mo-button type="primary" disabled :loading="true">
        <template #title>加载中</template>
      </mo-button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  components: {},
  methods: {},
  mounted() {},
  watch: {},
  computed: {},
  filters: {}
};
</script>

<style scoped lang='scss'>
.btn-box,
.btn-plain,
.btn-round,
.btn-icon,
.btn-disabled {
  width: 60%;
  margin-bottom: 20px;
}
</style>