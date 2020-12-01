# css预处理器

## 作用

- 嵌套层级和约束
- 变量和计算 
- Extend Mixin 代码片段
- 循环
- import css文件模块化


## less

### 嵌套

### 变量

```css
@fontSize: 12px;
@bgColor: red;
```

### mixin

```css
.block(@fontSize){
    font-size: @fontSize;
    border: 1px solid #ccc;
    border-radius: 4px;
}

.block(@fontSize);
```


### extend

```css
.nav:extend(.block){}
```

### 循环 loop

```css
.gen-col(@n) when (@n > 0){
    .gen-col(@n - 1);
    .col-@{n}{
        width: 1000px/12*@n;
    }
}

.gen-col(12);
```



### import



## sass

### 嵌套

### 变量
```css
$fontSize: 12px;
$bgColor: red;
```


### mixin


```css
@mixin block($fontSize){
    font-size: $fontSize;
    border: 1px solid #ccc;
    border-radius: 4px;
}

@include block($fontSize);
```


### extend

```css
 @extend .block;
```

### 循环 loop

```css

// @mixin gen-col($n){
//     @if $n > 0 {
//         @include gen-col($n - 1);
//         .col-#{$n}{
//             width: 1000px/12*$n;
//         }
//     }
// }

// @include gen-col(12);


@for $i from 1 through 12 {
    .col-#{$i} {
        width: 1000px/12*$i;
    }
}

```


### import



## 预处理器框架

> 按需使用其他人的代码

- SASS-Compass
- Less-Lesshat/EST
- 提供现成的mixin
- 类似js类库，封装常用的功能 