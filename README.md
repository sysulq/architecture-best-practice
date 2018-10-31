# architecture-best-practice
Best practice from the ground up.

## 技术选型
* 前端：vue，elem，nodejs（页面渲染）
* 接口层：golang，protobuf，http，grpc
* 服务层：golang，protobuf，grpc
* 推送层：golang，websocket，grpc
* 数据层：mysql，redis，nsq

## 系统工具
* 版本控制：gitlab
* 代码发布：自研或基于go-pub改进
* 业务监控：prometheus
* 告警管理：prometheus alarm manager
* 配置管理：etcd，consul

## 接入架构
* lvs
* 外网nginx集群
* 内网nginx集群（支持http及grpc）
* 接口
* 服务
* 数据

  基于外网nginx集群做域名级别监控，内网nginx集群做接口级别监控

## 接口定义
* protobuf：包括http与grpc

  独立仓库统一管理protobuf，通过脚本实现包括规范检查，统一格式化及代码生成等
  
## 流程规范
* 需求分析
* 排期
* 定义接口protobuf
* 开发
* 联调
* 测试
* 上线（灰度或canary）
