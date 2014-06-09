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