# ToDo List

Todo List 是一个简单的任务列表，使用nodejs、express框架开发。目前只是实现了基本的功能，包括登录、注册、添加任务、查看任务、完成任务。

使用地址： [https://45.76.191.17/](https://45.76.191.17/)

### 如何部署项目

1 自行配置MonogoDB 数据库。演示项目的数据库使用docker部署 

```
docker run --name todoDB -p 127.0.0.1:4000:27017 -v /root/todo/data/db:/data/db -d mongo
```

2 下载代码、安装组件

```
git clone https://github.com/superzhan/ToDo.git
npm install
```
3 在根目录的monogoConfig.json文件中配置数据库地址和端口

```
{
  "host":"127.0.0.1",
  "port":27017,
  "database":"todo-api",
  "username":"super",
  "password":"super",
  "isAuth":false
}

```

4 运行

```
npm start
```
开发环境中可以用命令 `npm start` 运行项目。生产环境下可以安装pm2,用pm2 运行程序。

```
npm install -g pm2 
pm2 start process.json  // process.json 位于根目录，可以自行配置
```