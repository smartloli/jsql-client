# jsql-client
Intermediate DataSet use sql to query. http://smartloli.org

# Summary

If you want to sum up a set of data, go to the maximum, minimum, grouping, etc., need to customize the algorithm to complete these functions. Such as :
```bash
 [{"id":1,"name":"aaa","age":20},{"id":2,"name":"bbb","age":21},{"id":2,"name":"ccc","age":22},{}...]
```
## Traditional
```java
// ... Sum

long sum = 0L
for(int i=0;i<array.size();i++){
	JSONObject object = (JSONObject)array.get(i);
	sum += object.getLong("age");
}

// ...
```

## JSql Client
```java
// ... Use SQL

SELECT SUM(column) FROM TBL;

// ...
```

# Dependency
In ```pom.xml``` ，you can add follow context : 
```xml
<dependency>
	<groupId>org.smartloli</groupId>
	<artifactId>jsql-client</artifactId>
	<version>1.0.0</version>
</dependency>
```

# Developer
you can import ```JSqlUtils``` class, and use ```query``` method,like this :
```java
JSqlUtils.query(tabSchema, tableName, dataSets, sql);
```
