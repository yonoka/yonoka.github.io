﻿# TaskStatistics

任务统计信息

## 属性

| 名称        | 数据类型 | 说明                                                        |
| ----------- | -------- | ----------------------------------------------------------- |
| `startTime` | number   | 起始时间,单位：毫秒,以当天的 00:00:00 开始,最长时间为一个月 |
| `endTime`   | number   | 结束数据,单位：毫秒,以当天的 11:59:59 结束                  |
| `type`      | number   | 任务类型<br/>0 - 消杀<br/>1 - 回桩<br/>2 - 配送<br/>3 - 召唤<br/>默认-1 全部       |

## 示例

```json
{
  "startTime": 1682870400000,
  "endTime": 1685548799000,
  "type": -1
}
```
