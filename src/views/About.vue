<template>
  <div class="about">
    <h1>This is an about page</h1>
    <User
      v-for="item in userInfo"
      :userName="item.name"
      :age="item.age"
      :sex="item.sex"
      :id="item.id"
    ></User>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import User from '../components/user.vue'
interface peopleInfo {
  name: string
  age: number
  sex?: number
  id: number
}
@Component({
  name: 'aboutItem',
  components: {
    User
  }
})
export default class extends Vue {
  userInfo: Array<peopleInfo> = [
    {
      id: 1,
      name: 'aaa',
      age: 11,
      sex: 1
    },{
      id: 2,
      name: 'bbb',
      age: 22,
      sex: 1
    },{
      id: 3,
      name: 'ccc',
      age: 33,
      sex: 2
    },
  ]
}
</script>
