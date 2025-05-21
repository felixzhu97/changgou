# 畅购商城项目

## 项目概述

畅购商城是一个基于 Spring Cloud 的分布式电商系统，包含商品管理、订单管理、用户管理等模块。

## 系统架构

采用微服务架构，主要包含以下组件：

- 服务注册中心：Eureka
- 配置中心：Spring Cloud Config
- 服务网关：Spring Cloud Gateway
- 业务服务：商品服务、订单服务等
- 数据库：MySQL 集群
- 缓存：Redis

## 模块说明

- changgou_common: 公共模块，包含通用工具类和 POJO
- changgou_eureka: 服务注册中心
- changgou_service: 业务服务模块
  - changgou_service_goods: 商品服务
- changgou_service_api: 服务 API 接口定义

## 技术栈

- 后端: Spring Boot, Spring Cloud, MyBatis
- 数据库: MySQL
- 注册中心: Eureka
- 构建工具: Maven

## 构建与运行

1. 安装 JDK 1.8 和 Maven
2. 克隆项目: `git clone [项目地址]`
3. 构建项目: `mvn clean install`
4. 启动 Eureka 服务: `cd changgou_eureka && mvn spring-boot:run`
5. 启动商品服务: `cd changgou_service/changgou_service_goods && mvn spring-boot:run`

## 数据库设计

- 商品数据库：包含品牌、分类、商品等表
- 使用 MyBatis 作为 ORM 框架
- 数据库脚本位置：/changgou_common_db/src/main/resources/sql/

## 开发环境要求

- JDK 1.8+
- Maven 3.6+
- MySQL 5.7+
- Redis 5.0+
- IDE 推荐：IntelliJ IDEA

## API 文档

- Swagger UI 地址：http://localhost:18081/swagger-ui.html
- 商品服务 API 文档：/changgou_service_api/changgou_service_goods_api/

## 贡献指南

1. Fork 本项目
2. 创建特性分支 (git checkout -b feature/xxx)
3. 提交修改 (git commit -am 'Add some feature')
4. 推送分支 (git push origin feature/xxx)
5. 创建 Pull Request

## 注意事项

- 运行前请确保已配置好数据库连接
- 默认端口:
  - Eureka: 8761
  - 商品服务: 18081
- 开发时请遵循阿里巴巴 Java 开发规范
