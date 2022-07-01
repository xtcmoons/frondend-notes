
json-server 集成到本地


#### 一, 进入项目目录，运行下面按照 json-server
```sh

 $ npm i json-server -D

```

#### 二，创建目录

```sh
$ mkdir __json_server_mock__

```

#### 三， 创建 db.json 文件

```sh
$ touch db.json
```


#### 四， 建立脚本命令

在package.json文件，scripts 下建立如下命令

```json
"scripts": {
    "start": "react-app-rewired start",
    "build": "react-app-rewired build",
    "test": "react-app-rewired test",
    "eject": "react-scripts eject",
    "json-server": "json-server __json_server_mock__/db.json --watch"
  },

```

json-server 只是个名字， 可以顺便取

#### 五， 运行脚本

```sh
$ npm run json-server
```

