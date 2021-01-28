# PDI-tutorials

PDI 原水壶 Kettle，这里是我学习和练习 PDI 的一些记录。


官网：https://www.hitachivantara.com/en-hk/products/data-management-analytics/pentaho-platform/pentaho-data-integration.html

社区版下载地址：https://sourceforge.net/projects/pentaho/

## Tutorials_1
一个简单的例子将数据从 Table_1 保存到 Table_2。

* [练习1 B站](https://b23.tv/SJPOp9)

* [练习1 西瓜视频](https://v.ixigua.com/JpFBvas/)

## Tutorials_2

加载 Excel 文件，保存到另外一个 Excel 文件和数据库表Table_2中。

* [练习2 B站](https://www.bilibili.com/video/BV1Tp4y1B7Be/)

* [练习2 西瓜视频](https://www.ixigua.com/i6911320394481795584/)

## Tutorials_3

加载 Json 文件，保存到另外一个 Json 文件和数据库表Table_2中。
* [练习3 B站](https://www.bilibili.com/video/BV1Ky4y1U7iG/)

* [练习3 西瓜视频](https://www.ixigua.com/i6911857625093112320/)

## Tutorials_4

REST接口的访问：通过访问新浪热刺接口，将热点新闻保存到数据库中。
* [练习4 B站](https://www.bilibili.com/video/BV12K4y157U2)

* [练习4 西瓜视频](https://www.ixigua.com/i6915605345972781568/)

## Tutorials_5

JavaScript 脚本：在 PDI 中使用 JavaScript 脚本处理数据。
* [练习5 B站](https://www.bilibili.com/video/BV1xX4y1K7WF)

* [练习5 西瓜视频](https://www.ixigua.com/i6916878986651894287/)

## Tutorials_6

Java Code 脚本：在 PDI 中使用 Java Code 脚本处理数据。
* [练习6 B站](https://www.bilibili.com/video/BV1Wt4y1z7nH/)

* [练习6 西瓜视频](https://www.bilibili.com/video/BV1Wt4y1z7nH/)

## Tutorials_7

任务处理：在 PDI 中通过任务执行转换。
* [练习7 B站](https://www.bilibili.com/video/BV1D5411n7nw/)

* [练习7 西瓜视频](https://www.ixigua.com/i6917614317328466432/)

## Tutorials_8

任务处理：在 PDI 中通过任务执行转换。
* [练习8 B站](https://www.bilibili.com/video/BV1A5411H78J/)

* [练习8 西瓜视频](https://www.ixigua.com/i6918010742113305088/)

## Tutorials_9

参数应用：在 PDI 中如何使用参数。
* [练习9 B站](https://www.bilibili.com/video/BV17N411d7uN/)

* [练习9 西瓜视频](https://www.ixigua.com/i6918389926182519296/)

## Tutorials_10

并行运行： 每个步骤都是并行运行的

* [练习10 B站](https://www.bilibili.com/video/BV1nz4y1S7aB/)

* [练习10 西瓜视频](https://www.ixigua.com/i6921331203853255183/)
## Tutorials_11

同步执行：如何同步执行转换

* [练习9 B站](https://www.bilibili.com/video/BV1A5411H78J/)

* [练习9 西瓜视频](https://www.ixigua.com/i6918010742113305088/)
## Tutorials_12

二次开发： 二次开发环境搭建

* [练习9 B站](https://www.bilibili.com/video/BV1A5411H78J/)

* [练习9 西瓜视频](https://www.ixigua.com/i6918010742113305088/)

先手动将开发库添加到本地仓库：

```
mvn install:install-file -Dfile=kettle-core-9.1.0.0-324.jar  -DgroupId=pentaho-kettle -DartifactId=kettle-core -Dversion=9.1.0.0-324 -Dpackaging=jar
mvn install:install-file -Dfile=kettle-engine-9.1.0.0-324.jar  -DgroupId=pentaho-kettle -DartifactId=kettle-engine -Dversion=9.1.0.0-324 -Dpackaging=jar
mvn install:install-file -Dfile=kettle-ui-swt-9.1.0.0-324.jar  -DgroupId=pentaho-kettle -DartifactId=kettle-ui-swt -Dversion=9.1.0.0-324 -Dpackaging=jar
mvn install:install-file -Dfile=kettle-dbdialog-9.1.0.0-324.jar  -DgroupId=pentaho-kettle -DartifactId=kettle-dbdialog -Dversion=9.1.0.0-324 -Dpackaging=jar
mvn install:install-file -Dfile=metastore-9.1.0.0-324.jar  -DgroupId=pentaho-kettle -DartifactId=kettle-metastore -Dversion=9.1.0.0-324 -Dpackaging=jar
mvn install:install-file -Dfile=kettle-log4j-core-9.1.0.0-324.jar  -DgroupId=pentaho-kettle -DartifactId=kettle-log4j-core -Dversion=9.1.0.0-324 -Dpackaging=jar
mvn install:install-file -Dfile=pentaho-encryption-support-9.1.0.0-324.jar  -DgroupId=pentaho-kettle -DartifactId=kettle-encryption-support -Dversion=9.1.0.0-324 -Dpackaging=jar
mvn install:install-file -Dfile=commons-lang-2.6.jar  -DgroupId=org.apache.commons -DartifactId=org.apache.commons.lang -Dversion=2.6 -Dpackaging=jar
```

pom.xml 文件参考：

```
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
	<modelVersion>4.0.0</modelVersion>
	<parent>
		<groupId>org.springframework.boot</groupId>
		<artifactId>spring-boot-starter-parent</artifactId>
		<version>2.3.4.RELEASE</version>
		<relativePath/> <!-- lookup parent from repository -->
	</parent>
	<groupId>com.khidi</groupId>
	<artifactId>sync</artifactId>
	<version>0.1</version>
	<name>sync</name>
	<description>Demo project for Spring Boot</description>

	<properties>
		<java.version>1.8</java.version>
		<pdi.version>9.1.0.0-324</pdi.version>
		<maven.test.skip>true</maven.test.skip>
	</properties>

	<!-- 
	<repositories>
	    <repository>
	        <id>pentaho-releases</id>
	        <url>https://nexus.pentaho.org/content/groups/omni</url>
	        <url>http://repository.pentaho.org/artifactory/repo/</url>
	    </repository>
	</repositories>
	-->
	<repositories>
		<repository>
			<id>spring-milestones</id>
			<name>Spring Milestones</name>
			<url>https://repo.spring.io/milestone</url>
			<snapshots>
				<enabled>false</enabled>
			</snapshots>
		</repository>
		<repository>
			<id>jcenter-snapshots</id>
			<name>jcenter</name>
			<url>http://oss.jfrog.org/artifactory/oss-snapshot-local/</url>
		</repository>
	</repositories>
	
	<dependencies>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter</artifactId>
			<!-- 
			<exclusions>
	          <exclusion>
	            <groupId>org.springframework.boot</groupId>
	            <artifactId>spring-boot-starter-logging</artifactId>
	          </exclusion>
	        </exclusions>
	         -->
		</dependency>	
		<dependency>
			<groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-logging</artifactId>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-jersey</artifactId>
		</dependency>
		<!-- 
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		 -->
		<!-- https://mvnrepository.com/artifact/pentaho-kettle/kettle-core -->
		<dependency>
		    <groupId>pentaho-kettle</groupId>
		    <artifactId>kettle-core</artifactId>
		    <version>${pdi.version}</version>
		</dependency>
		
		<!-- https://mvnrepository.com/artifact/pentaho-kettle/kettle-engine -->
		<dependency>
		    <groupId>pentaho-kettle</groupId>
		    <artifactId>kettle-engine</artifactId>
		    <version>${pdi.version}</version>
		</dependency>
		
		<!-- https://mvnrepository.com/artifact/pentaho-kettle/kettle-ui-swt -->
		<dependency>
		    <groupId>pentaho-kettle</groupId>
		    <artifactId>kettle-ui-swt</artifactId>
		    <version>${pdi.version}</version>
		</dependency>
		
		<!-- https://mvnrepository.com/artifact/pentaho-kettle/kettle-db -->
		<dependency>
		    <groupId>pentaho-kettle</groupId>
		    <artifactId>kettle-dbdialog</artifactId>
		    <version>${pdi.version}</version>
		</dependency>
		<dependency>
		    <groupId>pentaho-kettle</groupId>
		    <artifactId>kettle-metastore</artifactId>
		    <version>${pdi.version}</version>
		</dependency>
		<dependency>
		    <groupId>pentaho-kettle</groupId>
		    <artifactId>kettle-log4j-core</artifactId>
		    <version>${pdi.version}</version>
		</dependency>
		<dependency>
		    <groupId>pentaho-kettle</groupId>
		    <artifactId>kettle-encryption-support</artifactId>
		    <version>${pdi.version}</version>
		    <!-- <systemPath>D:/app/data-integration/lib/pentaho-encryption-support-9.1.0.0-324.jar</systemPath> -->
		</dependency>
		<!-- https://mvnrepository.com/artifact/log4j/log4j -->
		<dependency>
		    <groupId>log4j</groupId>
		    <artifactId>log4j</artifactId>
		    <version>1.2.17</version>
		</dependency>
		
		<!-- https://mvnrepository.com/artifact/org.apache.commons/commons-lang3 -->
		<dependency>
		    <groupId>org.apache.commons</groupId>
		    <artifactId>commons-lang3</artifactId>
		    <version>3.11</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/commons-lang/commons-lang -->
		<dependency>
		    <groupId>commons-lang</groupId>
		    <artifactId>commons-lang</artifactId>
		    <version>2.6</version>
		</dependency>

		<!-- https://mvnrepository.com/artifact/org.apache.commons/commons-vfs2 -->
		<dependency>
		    <groupId>org.apache.commons</groupId>
		    <artifactId>commons-vfs2</artifactId>
		    <version>2.6.0</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/org.apache.commons/commons-collections4 -->
		<dependency>
		    <groupId>org.apache.commons</groupId>
		    <artifactId>commons-collections4</artifactId>
		    <version>4.4</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/commons-collections/commons-collections -->
		<dependency>
		    <groupId>commons-collections</groupId>
		    <artifactId>commons-collections</artifactId>
		    <version>3.2.2</version>
		</dependency>
		
		<!-- https://mvnrepository.com/artifact/com.google.guava/guava -->
		<dependency>
		    <groupId>com.google.guava</groupId>
		    <artifactId>guava</artifactId>
		    <version>29.0-jre</version>
		</dependency>

		<!-- https://mvnrepository.com/artifact/commons-io/commons-io -->
		<dependency>
		    <groupId>commons-io</groupId>
		    <artifactId>commons-io</artifactId>
		    <version>2.8.0</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/commons-codec/commons-codec -->
		<dependency>
		    <groupId>commons-codec</groupId>
		    <artifactId>commons-codec</artifactId>
		    <version>1.15</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/javax.xml.ws/jaxws-api -->
		<dependency>
		    <groupId>javax.xml.ws</groupId>
		    <artifactId>jaxws-api</artifactId>
		    <version>2.3.1</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/com.sun.jersey.contribs/jersey-apache-client4 -->
		<dependency>
		    <groupId>com.sun.jersey.contribs</groupId>
		    <artifactId>jersey-apache-client4</artifactId>
		    <version>1.19.4</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/org.scannotation/scannotation -->
		<dependency>
		    <groupId>org.scannotation</groupId>
		    <artifactId>scannotation</artifactId>
		    <version>1.0.3</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/com.googlecode.json-simple/json-simple -->
		<dependency>
		    <groupId>com.googlecode.json-simple</groupId>
		    <artifactId>json-simple</artifactId>
		    <version>1.1.1</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/org.eclipse.birt.runtime.3_7_1/org.mozilla.javascript -->
		<dependency>
		    <groupId>org.eclipse.birt.runtime.3_7_1</groupId>
		    <artifactId>org.mozilla.javascript</artifactId>
		    <version>1.7.2</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/com.sun.mail/javax.mail -->
		<dependency>
		    <groupId>com.sun.mail</groupId>
		    <artifactId>javax.mail</artifactId>
		    <version>1.6.2</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/org.apache.poi/poi -->
		<dependency>
		    <groupId>org.apache.poi</groupId>
		    <artifactId>poi</artifactId>
		    <version>3.17</version>
		</dependency>
		
		<!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
		<dependency>
		    <groupId>mysql</groupId>
		    <artifactId>mysql-connector-java</artifactId>
		    <version>5.1.49</version>
		</dependency>
		<!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
		<dependency>
		    <groupId>mysql</groupId>
		    <artifactId>mysql-connector-java</artifactId>
		    <version>8.0.22</version>
		</dependency>
		<dependency>
		    <groupId>com.oracle</groupId>
		    <artifactId>ojdbc6</artifactId>
		    <version>12.1.0.1-atlassian-hosted</version>
		</dependency>
		
		<dependency>
			<groupId>com.microsoft.sqlserver</groupId>
			<artifactId>mssql-jdbc</artifactId>
			<!--<version>7.0.0.jre8</version> -->
		</dependency>
		<dependency>
			<groupId>com.github.ulisesbocchio</groupId>
			<artifactId>jasypt-spring-boot-starter</artifactId>
			<version>3.0.3</version>
		</dependency>
		<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
			<exclusions>
				<exclusion>
					<groupId>org.junit.vintage</groupId>
					<artifactId>junit-vintage-engine</artifactId>
				</exclusion>
			</exclusions>
		</dependency>
	</dependencies>

	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>
			<plugin>
			  <groupId>com.github.ulisesbocchio</groupId>
			  <artifactId>jasypt-maven-plugin</artifactId>
			  <version>3.0.3</version>
			</plugin>
		</plugins>
	</build>

</project>

```

> 二次开发参考：
> * https://help.pentaho.com/Documentation/8.2/Developer_Center/PDI/Embed
> * https://wiki.pentaho.com/pages/viewpage.action?pageId=13175504
> * https://jaxenter.com/run-pdi-based-etl-java-154655.html