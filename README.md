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


####Button Group（CSS）

#####支持的tag
`div`

#####简介
把`button`控件分组起来。

#####功能介绍
1. button group把button组合成一行。
2. button group可以为组内button提供类似checkbox或者radio行为。可以选中一个或者多个。

#####HTML

######普通group
    <div class="ui-button-group">
      <button class="ui-button primary">
      </button>
      <button class="ui-button secondary">
      </button>
    </div>

######像checkbox一样的group，选中一个后button变成active状态。
    <div class="ui-button-group">
      <button class="ui-button primary checkbox">
      </button>
      <button class="ui-button secondary checkbox">
      </button>
    </div>

######像radio一样的group，选中button变成active状态。
    <div class="ui-button-group">
      <button class="ui-button primary radio">
      </button>
      <button class="ui-button secondary radio">
      </button>
    </div>

####Button Bar（CSS）
#####支持的tag
`div`

#####简介
把`button group`组合起来。

#####功能介绍
1. button group横向排列；

#####HTML
    <div class="ui-button-toolbar" role="toolbar">
      <div class="ui-button-group">...</div>
      <div class="ui-button-group">...</div>
      <div class="ui-button-group">...</div>
    </div>
    
    

####Inputbox（CSS）

#####简介
输入框

#####功能介绍
1. 可以支持多个尺寸。

#####HTML
    <input class="ui-text mini" />

####Inputbox Group（CSS）
#####简介
`Input Group`

#####功能介绍
1. 可以在`Input Box`前后添加button，icon，或者文字

#####HTML
    <div class="input-group">
      <span class="input-group-addon">$</span>
      <input type="text" class="form-control">
      <span class="input-group-addon">.00</span>
    </div>


####Select（JS）
#####支持的tag
`select`
#####简介
下拉框

#####功能介绍
1. 把select变成一个DOM组成的下拉列表。
2. 下拉列表中可以支持过滤功能。
3. 下拉中空值value，作为默认选项。

#####HTML
    <select>
        <option value="">请选择</option>
        <option value="1">选项1</option>
    </select>

####Auto Complete
#####支持的tag
`input`, `textarea`
#####简介
自动搜索或者过滤列表，帮助用户完成输入。
#####功能介绍
1. 支持静态列表。
2. 支持ajax请求远程列表。
3. 列表要支持html 模版。


####多选列表
#####支持的tag
`select` multiple type
#####简介
下拉列表，输入过滤列表，可以选择多个值。
#####功能介绍
#####HTML

####日期控件
#####支持的tag
`input`
#####简介
选择日期
#####功能介绍
1. 可以指定日期格式。
2. 可以指定关联的日期控件。验证开始和结束。
3. 可以指定关联的时间控件

#####HTML


####提示气泡（ESUI的toaster）
#####支持的tag
#####简介
提示信息。
#####功能介绍
1. 分为info,error,warning,success,default
2. 可以设置提示自动关闭时间。

#####HTML


####Dialog
#####支持的tag
#####简介
现实页面信息框
#####功能介绍
1. 提示图标Error，Question，Infomation，Warning
2. Buttons设置，OKCancel，YesNo
#####HTML

####Checkbox&Radio
#####支持的tag
`Checkbox`
#####简介
为用户提供多选
#####功能介绍
1. 横向排列。
2. 纵向排列。
3. 自定义皮肤。
4. 支持toggle样式的皮肤。(Checkbox)

#####HTML


####Breadcrumbs
#####支持的tag
#####简介
导航面包屑
#####功能介绍
1. 横向复杂面包屑。
2. 简单面包屑。

#####HTML

####Grid&List Table
#####支持的tag
#####简介
数据表格
#####功能介绍
重点

#####HTML


####Tooltip
#####支持的tag
#####简介
标准Tooltip的替代品。
#####功能介绍
1. 位置；
2. 动画；

#####HTML

####Dual-List
#####支持的tag
`select` multiple type
#####简介
双向选择列表。
#####功能介绍
1. 支持group。
2. 支持列表过滤。
3. 支持全选，删除全部。

#####HTML

####Dual－Tree-List
#####支持的tag
`Input`
#####简介
双向树状选择列表。
#####功能介绍
1. 左侧树状选择。
2. 支持树查找，过滤。
3. 支持全选，删除全部。

#####HTML


####MultipleSelect
#####支持的tag
`Select` multiple type
#####简介
多选列表。[类似Telerik](http://demos.telerik.com/aspnet-mvc/multiselect/index)
#####功能介绍

#####HTML


####Progress Bar
#####支持的tag
`div`
#####简介
进度条
#####功能介绍
1. 动画。

#####HTML

####Uploader
#####支持的tag
`div`
#####简介
上传,[上传文件]（http://blueimp.github.io/jQuery-File-Upload/）
#####功能介绍
1. 上传单个。
2. 上传多个。
3. 进度条显示。
4. 预览。
5. 文件类型检测。

#####HTML


####Input Mask
#####支持的tag
`input`
#####简介
对输入进行限制。[MaskedInput](http://demos.telerik.com/aspnet-mvc/maskedtextbox/index)
#####功能介绍
#####HTML

####Numeric Input
#####支持的tag
`input`
#####简介
对数字输入提供支持。[NumericInput](http://demos.telerik.com/aspnet-mvc/numerictextbox/index)
#####功能介绍
#####HTML


####控件名称
#####支持的tag
#####简介
#####功能介绍
#####HTML
