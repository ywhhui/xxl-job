1、简单：支持通过Web页面对任务进行CRUD操作，操作简单，一分钟上手；
2、动态：支持动态修改任务状态、启动/停止任务，以及终止运行中任务，即时生效；
3、调度中心HA（中心式）：调度采用中心式设计，“调度中心”自研调度组件并支持集群部署，可保证调度中心HA；
4、执行器HA（分布式）：任务分布式执行，任务”执行器”支持集群部署，可保证任务执行HA；
5、注册中心: 执行器会周期性自动注册任务, 调度中心将会自动发现注册的任务并触发执行。同时，也支持手动录入执行器地址；
6、阻塞处理策略：调度过于密集执行器来不及处理时的处理策略，策略包括：单机串行（默认）、丢弃后续调度、覆盖之前调度；
7、任务超时控制：支持自定义任务超时时间，任务运行超时将会主动中断任务；
8、任务失败重试：支持自定义任务失败重试次数，当任务失败时将会按照预设的失败重试次数主动进行重试；其中分片任务支持分片粒度的失败重试；
9、任务失败告警；默认提供邮件方式失败告警，同时预留扩展接口，可方便的扩展短信、钉钉等告警方式；
10、任务进度监控：支持实时监控任务进度；
11、Rolling实时日志：支持在线查看调度结果，并且支持以Rolling方式实时查看执行器输出的完整的执行日志；
12、自定义任务参数：支持在线配置调度任务入参，即时生效；
13、数据加密：调度中心和执行器之间的通讯进行数据加密，提升调度信息安全性；
14、邮件报警：任务失败时支持邮件报警，支持配置多邮件地址群发报警邮件；
