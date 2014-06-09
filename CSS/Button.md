####Button（CSS）

#####支持的Tags
`input`, `button`, `anchor`

#####简介
交互的button。

#####功能介绍
1. button有几种主要颜色，primary，success，link，...；
2. button有不同的尺寸， mini, tiny, medium, large, huge, monster；
3. Hover动画？
4. button可以有一个icon；声明方式：·<button><span class="icon icon-plus"></span></button>·；
5. button可以以block形式显示，填充父元素；
5. button的状态：nomral, hover, down, active;
6. button可以是圆形或者圆角；

#####HTML

######`large`尺寸的`button`，颜色为`primary`，内部有一个`icon`
    <button class="ui-button primary large">
      <i class="icon icon-plus"></i>
      Create
    </button>

######圆形`button`
    <button class="ui-button primary large round">
      <i class="icon icon-plus"></i>
    </button>
