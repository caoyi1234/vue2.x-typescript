<template>
  <div>
    id:{{id}}
    姓名:{{userName}}
    性别:{{SEX[sex]}}
    年龄:{{age}}
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator'
@Component({
  name: 'User'
})
enum Sex {
  '男' = 1,
  '女' = 2
}

export default class User extends Vue {
  @Prop(Number)
  id!: number

  @Prop(String)
  userName!: string

  @Prop({ type: Number, default: 1 })
  sex?: number

  @Prop(Number)
  age!: number

  SEX: any = Sex
}
</script>
