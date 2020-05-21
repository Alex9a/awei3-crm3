<template>
  <div>
    <form-container
      :inline="true"
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
        :rules="formInputRules"
        v-roles="''"
      ></form-input>
      <form-input
        :in-container="true"
        type="number"
        placeholder="请输入"
        label="数字框"
        :is-label-visible="true"
        :status="0"
        :step="1"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules_1"
        v-roles="''"
      ></form-input>
      <form-input
        :in-container="true"
        type="number"
        placeholder="请输入"
        label="数字框"
        :is-label-visible="true"
        :status="0"
        :step="1"
        :min="2"
        :max="30"
        :require="false"
        :is-show-min="false"
        :is-show-max="false"
        :is-show-customer="false"
        :rules="formInputRules_2"
        v-roles="''"
      ></form-input>
    </form-container>
    <config-table
      name="基础表格"
      :visible="false"
      :pagination="configTablePagination"
      :is-operation="false"
      operation-name="操作"
      :table-data="configTableTabledata"
      :table-data-static="configTableTabledatastatic"
      :table-config="configTableTableconfig"
      :parameter-list="configTableParameterlist"
      v-roles="''"
    ></config-table>
    <ve-histogram
      :data="veHistogramData"
      :grid="veHistogramGrid"
      :legend="veHistogramLegend"
      height="300px"
      v-roles="''"
    ></ve-histogram>
  </div>
</template>
<script>
export default {
  components: {},
  data: function() {
    return {
      pageName: "个人中心",
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
      configTablePagination: [10],
      configTableTabledata: [{}],
      configTableTabledatastatic: [],
      configTableTableconfig: [
        {
          label: "序号",
          name: "index"
        },
        {
          label: "创建时间",
          name: "creatAt"
        },
        {
          label: "修改时间",
          name: "updateAt"
        },
        {
          label: "创建人",
          name: "createBy"
        }
      ],
      configTableParameterlist: [],
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
  methods: {},
  destroyed: function() {}
}
</script>
<style lang="less" scoped="scoped"></style>
