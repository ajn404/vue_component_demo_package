# 这是一个测试发版包

## 使用方法

```bash
yarn add vue_component_demo_package
```

```vue
<template>
  <div>
    <count-to></count-to>
  </div>
</template>
<script>
import CountTo from 'vue_component_demo_package';
export default {
  components:{
   CountTo
  }
}
</script>
```