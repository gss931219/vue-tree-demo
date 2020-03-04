<template>

  <div class="hello">
    <div><el-button @click="test()">点击</el-button></div>
    <tree
      :treeData="treeData"
      v-model="ids"
      :withoutParents="withoutParents"
      :options="treeOptions"
    ></tree>


    <div style="margin-top: 100px;">
      包含父节点的数组用这个ids[必填项]:{{ids}}
    </div>
    <div>
      不包含父节点的数组用这个withoutParents[非必填项]:{{withoutParents}}
    </div>
  </div>
</template>

<script>
import tree from '@/components/tree'
export default {
  name: 'HelloWorld',
  data () {
    return{
      ids:[34], //包含父节点
      withoutParents:[],  //不包含父节点
      treeOptions:{
      withParents:true  //是否包含父节点，如果为false,则要添加withoutParents这个参数，如果为true则不需要添加
    },
      treeData:[
          {
              "name":"产品中心",
              "id":10,
              "parentId":0,
              "child":[
                  {
                      "name":"产品管理",
                      "id":34,
                      "parentId":10,
                      "child":[

                      ]
                  },
                  {
                      "name":"模板管理",
                      "id":63,
                      "parentId":10,
                      "child":[

                      ]
                  }
              ]
          },
          {
              "name":"部件中心",
              "id":36,
              "parentId":0,
              "child":[
                  {
                      "name":"barebone",
                      "id":28,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"处理器",
                      "id":30,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"内存",
                      "id":38,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"硬盘背板",
                      "id":14,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"硬盘",
                      "id":16,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"PCIe插槽",
                      "id":18,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"PCIe板卡",
                      "id":19,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"电源",
                      "id":53,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"电源线",
                      "id":54,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"配件",
                      "id":55,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"软件",
                      "id":56,
                      "parentId":36,
                      "child":[

                      ]
                  },
                  {
                      "name":"价格管理",
                      "id":57,
                      "parentId":36,
                      "child":[

                      ]
                  }
              ]
          },
          {
              "name":"规则中心",
              "id":21,
              "parentId":0,
              "child":[
                  {
                      "name":"配件规则",
                      "id":61,
                      "parentId":21,
                      "child":[

                      ]
                  },
                  {
                      "name":"计算节点规则",
                      "id":62,
                      "parentId":21,
                      "child":[

                      ]
                  }
              ]
          },
          {
              "name":"运营中心",
              "id":46,
              "parentId":0,
              "child":[
                  {
                      "name":"用户反馈",
                      "id":58,
                      "parentId":46,
                      "child":[

                      ]
                  },
                  {
                      "name":"邮件列表",
                      "id":59,
                      "parentId":46,
                      "child":[

                      ]
                  }
              ]
          },
          {
              "name":"用户中心",
              "id":6,
              "parentId":0,
              "child":[
                  {
                      "name":"机构管理",
                      "id":35,
                      "parentId":6,
                      "child":[

                      ]
                  },
                  {
                      "name":"终端角色",
                      "id":8,
                      "parentId":6,
                      "child":[

                      ]
                  },
                  {
                      "name":"终端用户",
                      "id":9,
                      "parentId":6,
                      "child":[

                      ]
                  }
              ]
          },
          {
              "name":"管理中心",
              "id":1,
              "parentId":0,
              "child":[
                  {
                      "name":"角色管理",
                      "id":3,
                      "parentId":1,
                      "child":[

                      ]
                  },
                  {
                      "name":"用户管理",
                      "id":2,
                      "parentId":1,
                      "child":[

                      ]
                  },
                  {
                      "name":"个人管理",
                      "id":60,
                      "parentId":1,
                      "child":[

                      ]
                  },
                  {
                      "name":"系统日志",
                      "id":7,
                      "parentId":1,
                      "child":[

                      ]
                  },
                  {
                      "name":"权限管理",
                      "id":4,
                      "parentId":1,
                      "child":[

                      ]
                  },
                  {
                      "name":"菜单管理",
                      "id":5,
                      "parentId":1,
                      "child":[

                      ]
                  }
              ]
          }
      ]
    }
  },
  methods:{
    test(){
      debugger
      this.ids = [28]
    }
  },
  components: {
    'tree':tree
  }
}
</script>

<style>
  li{list-style:none;vertical-align:top;}
</style>
