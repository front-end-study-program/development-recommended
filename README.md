# development-recommended
前端实际开发推荐用法

## scss
1. @mixin 封装公共的混入规则，来简化代码
``` scss
// 定义
@mixin flexBox( $directionVlaue: row, $justifyValue: flex-start, $alignValue: baseline ) {
  display: flex;
  flex-direction: $directionVlaue;
  justify-content: $justifyValue;
  align-items: $alignValue;
}

// 使用
.thing {
   @include flexBox(row, center, center);
}
// 跳过默认值
.thing {
   @include flexBox( , center, center); // leave first argument empty
}
```
