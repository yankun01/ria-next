ria-next
========

用于讨论下一代RIA体系，讨论采纳的功能将在合适的版本中进行实现

讨论可包含并不限于：[ER](https://github.com/ecomfe/er)、[ESUI](https://github.com/ecomfe/esui)、[etpl](https://github.com/ecomfe/etpl)及相关的工具、类库

##ESUI

###概述
在[ESUI](https://github.com/ecomfe/esui)现有控件的基础上：
1. 加入CSS框架，为基础HTML控件和HTML组合控件提供样式支持，并提供CSS Grid。
2. 对现有ESUI控件进行进一步设计，优化和整理。
3. 添加通用的组件。


###目标
1. 提供一套功能设计优良，功能稳定的标准控件和交互行为。
2. 提供一个Sytle Guide页面列出所有的设计组件。
3. UE可能自行定义标准样式给FE使用。

###加强点
1. 加入CSS基础框架。
2. 加入CSS grid。
3. 尝试剥离控件对icon的依赖，可以使用image icon或者web font。
4. 搜集业务需求，在现有ESUI基础上，对其功能进行一点功能。通过option来提供。
5. 添加一些通用的组件进来。
6. 对控件添加Unit Test来进一步保证质量。
7. 动画[CSS Animation](http://daneden.github.io/animate.css/)。可以实现类似于[groundwork](http://groundworkcss.github.io/)的效果。

###关于AMD
可以使用AMD也可以不使用。
[UMD](https://github.com/umdjs/umd/blob/master/amdWeb.js)

###组件分类
组件可以分为以下几种类型：

1. HTML基础控件。（CSS目录下）
2. HTML组合控件。（Components目录下）
3. 可复用CSS View。（View目录下）
4. JS组件。（JS目录下）
5. JS行为扩展。（Behavior目录下）


####HTML基础控件
HTML基础控件是基本页面元素, 代表一个独立的功能。例如Button，Input, Progress Bar。

####HTML组合控件
由一组HTML Tag组成的一个页面元素。例如：Inputs Group，Tool Bar，Form， Menu， Nav bar, Breadcrumbs。

####可复用CSS View
UI设计上更高一级的可以复用的一组HTML组合。由HTML基础控件和HTML组合控件组成。例如：List，关键词过滤列表等。

####JS组件
JS扩展的组件。例如现有的Calendar，Select等组件。

####JS行为扩展
JS的扩展行为。比如：Drag&Drop，Transition，Position等。

####控件和行为设计模板说明
| 控件定义名称 | 说明                                                                                |
|--------|-----------------------------------------------------------------------------------|
| 控件实现   | 每种控件可以有多个实例，分别表示不同的控件实现。例如：Button可以有带图标Button。Label可以有Ribbon Label，Corner Label等。 |
| 控件皮肤   | 每个控件实现可以包含多个皮肤，可以修改控件实现的外观。例如：普通Button可以红色，绿色，大的，小的几种皮肤。                          |
| 控件状态   | 该控件拥有的状态。例如：disabled，active，hovered，pressed down...                               |
| 控件行为   | 控件行为的说明。                                                                          |
| 控件属性   | 控件支持的属性。                                                                          |
| 实例     | HTML或者JS实例。说明如何使用。                                                                |
