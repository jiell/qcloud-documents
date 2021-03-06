腾讯云云监控为消息队列 CKafka 实例提供以下监控指标：

| 指标中文名         | 指标英文名          | 指标含义                                     | 单位   | 维度             |
| ------------- | -------------- | ---------------------------------------- | ---- | -------------- |
| 生产流量          | pro_flow       | 实例的实际生产流量（不包含副本产生的流量），按照所选择的时间粒度统计求和  | MB   | 实例             |
| 消费流量          | con_flow       | 实例的实际消费流量（不包含副本产生的流量），按照所选择的时间粒度统计求和  | MB   | 实例             |
| 已占用磁盘容量      | msg_heap      | 实例的落盘消息总量，按照所选择的时间粒度取最新值               | MB   | 实例             |
| 生产条数          | pro_count      | 实例的实际生产消息条数，按照所选择的时间粒度统计求和                | 条    | 实例             |
| 消费条数          | con_count      | 实例的实际消费消息条数，按照所选择的时间粒度统计求和                | 条    | 实例             |
| 生产请求的次数       | pro_req_count  | 实例级别生产请求次数，按粒度（1分钟、5分钟）统计求和              | 条    | 实例             |
| 消费请求的次数       | con_req_count  | 实例级别消费请求次数，按粒度（1分钟、5分钟）统计求和              | 条    | 实例             |
| 落盘消息条数        |  msg_count           | 实例的落盘消息总条数，按照所选择的时间粒度取最新值              | 条    | 实例             |
| 生产峰值带宽     | max_pro_flow           | 实例生产消息时产生的最大流量（不包含副本产生的流量）           | MB/s | 实例               |
| 消费峰值带宽     | max_con_flow               | 实例消费消息时产生的最大流量（消费时无副本的概念）             | MB/s | 实例            |
| 磁盘使用百分比   | disk_usage                | 当前磁盘占用与实例规格磁盘总容量的百分比                       | %    | 实例           |
| 生产流量          | pro_flow       | Topic 的实际生产流量（不包含副本产生的流量），按照所选择的时间粒度统计求和     | MB   | Topic       |
| 消费流量          | con_flow       | Topic 的实际消费流量（不包含副本产生的流量），按照所选择的时间粒度统计求和     | MB   | Topic       |
| 已占用磁盘容量     | msg_heap      | Topic 实际占用磁盘的消息总量（不包含副本），按照所选择的时间粒度取最新值      | MB   | Topic       |
| 生产条数          | pro_count      | Topic 的实际生产消息条数，按照所选择的时间粒度统计求和          | 条    | Topic          |
| 消费条数          | con_count      | Topic 的实际生产消息条数，按照所选择的时间粒度统计求和            | 条    | Topic          |
| 生产请求的次数       | pro_req_count  | Topic 级别生产请求次数，按粒度（1分钟、5分钟）统计求和           | 条    | Topic          |
| 消费请求的次数       | con_req_count  | Topic 级别消费请求次数，按粒度（1分钟、5分钟）统计求和           | 条    | Topic          |
| 落盘消息条数        |   msg_count       | Topic 的实际的落盘的消息总条数（不包含副本），按照所选择的时间粒度取最新值   | 条    | Topic          |
| 当前分区最大offset    | max_offset     | 消费分组对应当前 Topic 最大offset                                 | 条    | consumer group |
| 当前消费 offset       | offset         | 消费分组当前消费 offset                                          | 条    | consumer group |
| 未消费的消息条数      | unconsume      |消费分组未消费消息数                                              | 条    | consumer group |
| 未消费消息堆积量 | unconsume_size | 消费分组对应 partition 未被消费的消息总大小，按粒度（1分钟、5分钟）取最新值 | MB | consumer group |


关于如何使用消息队列 CKafka 的监控指标内容，请查看云监控 API 中的 [读取监控数据接口](https://cloud.tencent.com/document/api/248/4667)。
