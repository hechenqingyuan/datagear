# 数据齿轮 DataGear

数据齿轮（DataGear）是一款数据库管理系统，使用Java语言开发，采用浏览器/服务器架构，以数据管理为核心功能，支持多种数据库。

它的数据模型并不是原始的数据库表，而是融合了数据库表及表间关系，更偏向于领域模型的数据模型，能够更友好、方便、快速地查询和维护数据。

它采用JDBC规范与数据库进行连接和通信，能够支持所有遵循JDBC规范的数据库，这包括MySQL、Oracle、PostgreSQL、SQL Server等主流数据库。

## 官网

[http://www.datagear.tech](http://www.datagear.tech)

## 文档

[http://www.datagear.tech/documentation](http://www.datagear.tech/documentation)

## 界面

数据管理

![界面图片](http://datagear.tech/static/theme/lightness/images/datagear-home-screen.png)

SQL工作台

![界面图片](http://datagear.tech/static/theme/lightness/images/datagear-sqlpad-screen.png)

数据导入

![界面图片](http://datagear.tech/static/theme/lightness/images/datagear-dataimport-screen.png)

数据导出

![界面图片](http://datagear.tech/static/theme/lightness/images/datagear-dataexport-screen.png)

## 依赖

	Java 6+
	Servlet 3.0+

## 编译

	（执行单元测试编译，需要预先配置单元测试环境）
	mvn clean package


	（不执行单元测试编译，无需预先配置单元测试环境）
	mvn clean package -DskipTests

## 运行

	cd datagear-webembd/target/datagear-[version]
	
	（Linux环境）
	./startup.sh
	
	（windows环境）
	startup.bat

## 版本号升级

1. 修改`pom.xml`文件中的`version`标签内的版本号；

2. 执行如下maven命令：

		mvn -N versions:update-child-modules antrun:run

