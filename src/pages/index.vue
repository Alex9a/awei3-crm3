<template>
  <div>
    <div class="columns_3" style="width: 60%" v-roles="''" v-if="visible">
      <config-text
        :size="12"
        :weight="false"
        :italic="false"
        :underline="false"
        color="#000"
        vertical="left"
        inner-text="这是文本"
        :url_type="0"
        :page_new_window="false"
        :href_new_window="false"
        v-roles="''"
        class="text_1"
      ></config-text>
      <form-input
        type="text"
        placeholder="请输入"
        label="单行文本"
        :is-label-visible="true"
        :status="0"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules"
        v-roles="''"
      ></form-input>
    </div>
    <form-container
      :inline="false"
      position="left"
      primary-text="搜索"
      :have-second="true"
      second-text="重置"
      v-roles="''"
    >
      <form-input
        :in-container="true"
        type="text"
        placeholder="请输入"
        label="单行文本"
        :is-label-visible="true"
        :status="0"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules_1"
        v-roles="''"
      ></form-input>
    </form-container>
    <form-input
      type="text"
      placeholder="请输入"
      label="单行文本"
      :is-label-visible="true"
      :status="0"
      :min="2"
      :max="30"
      :require="false"
      :is-show-min="false"
      :is-show-max="false"
      :is-show-customer="false"
      :rules="formInputRules_2"
      v-roles="''"
    ></form-input>
    <form-input
      type="text"
      placeholder="请输入"
      label="单行文本"
      :is-label-visible="true"
      :status="0"
      :min="2"
      :max="30"
      :require="false"
      :is-show-min="false"
      :is-show-max="false"
      :is-show-customer="false"
      :rules="formInputRules_3"
      v-roles="''"
    ></form-input>
    <ve-histogram
      :data="veHistogramData"
      :grid="veHistogramGrid"
      :legend="veHistogramLegend"
      height="300px"
      v-roles="''"
    ></ve-histogram>
    <config-button
      :radius="1"
      :plain="false"
      bg-color="#5D81F9"
      :size="12"
      :weight="false"
      :italic="false"
      :underline="false"
      color="#fff"
      vertical="center"
      inner-text="按钮"
      :url_type="0"
      :page_new_window="false"
      :href_new_window="false"
      v-roles="''"
      class="button_6"
    ></config-button>
  </div>
</template>
<script>
export default {
  components: {},
  data: function() {
    return {
      pageName: "首页",
      visible: true,
      formInputRules: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      formInputRules_1: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      formInputRules_2: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      formInputRules_3: [
        {
          required: false,
          message: "",
          trigger: []
        }
      ],
      veHistogramData: {
        columns: ["日期", "访问用户", "下单用户", "下单率"],
        rows: [
          {
            日期: "1/1",
            访问用户: 1393,
            下单用户: 1093,
            下单率: 32
          },
          {
            日期: "1/2",
            访问用户: 3530,
            下单用户: 3230,
            下单率: 26
          },
          {
            日期: "1/3",
            访问用户: 2923,
            下单用户: 2623,
            下单率: 76
          },
          {
            日期: "1/4",
            访问用户: 1723,
            下单用户: 1423,
            下单率: 49
          },
          {
            日期: "1/5",
            访问用户: 3792,
            下单用户: 3492,
            下单率: 32.3
          },
          {
            日期: "1/6",
            访问用户: 4593,
            下单用户: 4293,
            下单率: 78
          }
        ]
      },
      veHistogramGrid: {
        top: 35,
        bottom: 10
      },
      veHistogramLegend: {
        top: 5
      }
    }
  },
  mounted: function() {},
  watch: {},
  methods: {
    show: function() {
      this.visible = true
    }
  },
  destroyed: function() {}
}
</script>
<style lang="less" scoped="scoped">
.columns_3 {
  margin-bottom: 0px;
  margin-left: 0px;
  margin-right: 0px;
  margin-top: 41px;
}
.text_1 {
  display: inline-block;
  vertical-align: top;
}
.button_6 {
  display: inline-block;
  vertical-align: top;
}
</style>
