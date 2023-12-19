# TaskInfo

任务信息

## 属性

| 名称       | 数据类型                          | 说明                                                         |
| ---------- | --------------------------------- | ------------------------------------------------------------ |
| `name`     | string                            | 任务名称                                                     |
| `robotId`  | string                            | 机器人标识                                                   |
| `runNum`   | number                            | 任务执行次数<br/>默认为1；0 表示无限循环                     |
| `taskType` | number                            | 任务类型<br/>0 - 消杀<br/>1 - 回桩充电<br/>2 - 餐厅          |
| `runType`  | number                            | 运行类型<br/>0 - 定时消杀<br/>1 - 临时消杀<br/>20 - 快捷送餐<br/>21 - 多点送餐<br/>22 - 引领<br/>23 - 巡游<br/>24 - 返航<br/>25 - 充电桩 |
| `curPt`    | [TaskPoint](#/Define-TaskPoint)   | 机器人当前位置                                               |
| `taskPts`  | [TaskPoint](#/Define-TaskPoint)[] | 任务节点列表                                                 |
| `backPt`   | [TaskPoint](#/Define-TaskPoint)   | 可选；任务结束后返回的节点                                   |























