# 数据表兼容性方案

#### 删除字段

- 禁止删除正在使用的字段
- 需要反对确认服务提供方、服务消费方都不再需要该字段时才允许删除
- 对于已有业务值的字段，可以考虑备份原数据再删除



#### 新增字段

- 允许为NULL
- 提供默认值
- 应用端可根据字段是否上线制定兼容性方案
- 要考虑是否需要写脚本进行初始化
- 要考虑是否需要写脚本对新增字段之前的历史数据进行处理

#### 变更字段

- 优先考虑新增一个字段，而非直接变更原字段