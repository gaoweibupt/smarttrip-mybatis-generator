# smarttrip-mybatis-generator
根据数据库表自动生成dao.xml、mapper.java和domain对象。

这时一个独立的工程，我smarttrip项目的其他工程之间不存在依赖关系。

## 使用方法
1. 修改数据库连接信息。在`<jdbcConnection>`标签中。
2. 修改targetProject路径信息。存在三处，其属性名称为`targetProject`。
3. 修改数据库表和对应的domain对象信息。分别是`tableName`和`domainObjectName`的值。
4. 在工程上点击右键-->Run As-->Maven build。在弹出的对话框中找到Goals，在里面输入值：`mybatis-generator:generate`，点击`Run`。
5. 等步骤四结束之后，刷新工程，便可在`src/main/java`下看到生成的三个文件。
6. 将生成的三个文件拷贝到对应的smarttrip工程中便可。

其中步骤1和2一般是修改一次便可，步骤3是每针对一张表生成一次代码都要修改。
