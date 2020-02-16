## 环境和工具
- Mac
- Git、Ant、Idea
- Jdk8

## 项目下载和安装
#### 1、安装 Ant
Ant下载地址： http://ant.apache.org/bindownload.cgi
解压即可

#### 2、下载Zookeeper源码包
```
git clone https://github.com/apache/zookeeper.git
```

## 工程构建
#### 0、先切换到相应的版本,我这里用的 3.5.6，需要注意Zookeeper目录下需要一个 build.xml文件
```
git checkout remotes/origin/branch-3.5.6
```

#### 1、利用Ant将Zookeeper源码编译成Eclipse项目
```
ant eclipse
```
等待编译结果输出如下图，即表示成功：
![zookeeper编译结果](https://github.com/xinput123/images/blob/master/compile/zookeeper%E7%BC%96%E8%AF%91%E6%88%90%E5%8A%9F%E6%88%AA%E5%9B%BE.jpg)

#### 2、将代码导入到idea
![导入Zookeeper到idea](https://github.com/xinput123/images/blob/master/compile/idea%E5%AF%BC%E5%85%A5%E6%88%AA%E5%9B%BE)

#### 3、编译Zookeeper源码
在 pom文件中找到以下文件，注释
```
<plugin>
          <groupId>org.codehaus.mojo</groupId>
          <artifactId>properties-maven-plugin</artifactId>
          <version>1.0.0</version>
</plugin>
```
