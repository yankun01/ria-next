ria-next
========

用于讨论下一代RIA体系，讨论采纳的功能将在合适的版本中进行实现

讨论可包含并不限于：[ER](https://github.com/ecomfe/er)、[ESUI](https://github.com/ecomfe/esui)、[etpl](https://github.com/ecomfe/etpl)及相关的工具、类库

##ESUI

###概述
[ESUI](https://github.com/ecomfe/esui)中的控件已经实现独立运行，我们可以继续增强功能并增加新控件。提供给不同的业务系统进行使用。

###目标
提供一套功能稳定的标准控件和交互行为。
与UX约定设计控件范围，减少UX设计的自由度，最大程度的进行复用，节省开发时间。
实现UE自行配置标准控件颜色。

###加强点
1. 搜集其他项目中成功的控件并加入esui中。
2. 对esui中的控件进行功能加强，提供option来控制这些功能。
3. 对控件添加Unit Test来进一步保证质量。
4. 尝试剥离控件对icon的依赖。尝试引入web font。

###关于AMD
可以使用AMD也可以不使用。
[UMD](https://github.com/umdjs/umd/blob/master/amdWeb.js)


###控件和交互行为设计

####Button

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

####HTML

#####`large`尺寸的`button`，颜色为`primary`，内部有一个`icon`
    <button class="ui-button primary large">
      <i class="icon icon-plus"></i>
      Create
    </button>

#####圆形`button`
    <button class="ui-button primary large round">
      <i class="icon icon-plus"></i>
    </button>


###Button Group

####支持的tag
`div`

####简介
把`button`控件分组起来。

####功能介绍
1. button group把button组合成一行。
2. button group可以为组内button提供类似checkbox或者radio行为。可以选中一个或者多个。

####HTML

#####普通group
    <div class="ui-button-group">
      <button class="ui-button primary">
      </button>
      <button class="ui-button secondary">
      </button>
    </div>

#####像checkbox一样的group，选中一个后button变成active状态。
    <div class="ui-button-group">
      <button class="ui-button primary checkbox">
      </button>
      <button class="ui-button secondary checkbox">
      </button>
    </div>

#####像radio一样的group，选中button变成active状态。
    <div class="ui-button-group">
      <button class="ui-button primary radio">
      </button>
      <button class="ui-button secondary radio">
      </button>
    </div>

###Button Bar
####支持的tag
`div`

####简介
把`button group`组合起来。

####功能介绍
1. button group横向排列；

####HTML
    <div class="btn-toolbar" role="toolbar">
      <div class="btn-group">...</div>
      <div class="btn-group">...</div>
      <div class="btn-group">...</div>
    </div>



