# docker

簡介：軟體容器平台 可快速建立 測試 部署應用程式

## 基本概念

* 映像檔（Image）
* 容器（Container）
* 倉庫（Repository）

### 映像檔
輕量的、可執行的獨立軟體包 ，包含軟體運行所需的所有內容：代碼、運行時環境、系統工具、系統庫和設置。

### 容器
將軟體打包成標準化單元，以用於開發、交付和部署。

### 倉庫（Repository）
集中存放映像檔檔案的場所。


映像檔和容器就像類和實例

Docker是不攜帶作業系統的，所以Docker的應用就非常的輕巧。


Docker 容器通過 Docker 鏡像來創建，容器與鏡像的關係類似於面向對象編程中的對象與類。


## dockerfile
* 用途

用來定義容器內發生的事情，並具體說明要“複製”的文件，這樣做之後，就可以確保在Dockerfile中定義的應用程序構建成功，無論在任何地方都能以相同方式運行。
* 建立方式

在目標資料夾建立Dockerfile，並輸入需要的指令

### 基本語法
* 使用#來註釋
* FROM 指令告訴 Docker 使用哪個映像檔作為基底
* 接著是維護者的信息
* RUN開頭的指令會在建立中執行，比如安裝一個套件，在這裏使用 apt-get 來安裝了一些套件


## 指令

#### 檢查版本
```shell
$ docker --version

$ docker info
```



#### 拉取映像檔
```shell
$ docker pull 映像檔名稱
```


#### 搜尋映像檔
```shell=
$ docker search 映像檔名稱
```


#### 查看目前映像檔
```shell
1. $ docker image ls
2. $ docker images
```

#### 建立映像檔
```shell
$ docker build -t/--tag="映像檔名" 路徑

ex:$ docker build -t=hello .

映像檔名：hello
路徑：.(當前路徑)

-t：指定新的映像檔的使用者信息
```


#### 查看目前系統中容器
```shell
1. $ docker container ls -a

-a為顯示全部

2. $ docker ps
```

#### 執行應用程式
```shell
$ docker run [選項] 程式名
```
[選項大全](https://jiajially.gitbooks.io/dockerguide/content/chapter_fastlearn/docker_run/index.html)

### 以Docker ID 登入
```shell
$ docker login
```

### 管理類指令
```shell
$ docker config
$ docker image
$ docker container
$ docker network
$ docker node
$ docker plugin
$ docker secret
$ docker service
$ docker stack
$ docker swarm
$ docker system
$ docker trust
$ docker volume
```







## 參考資料
[docker入門](https://philipzheng.gitbook.io/docker_practice/)

[docker-tutorial](https://github.com/twtrubiks/docker-tutorial)

[dockerfile 學習筆記](https://hackmd.io/PnuGE_LtQhSArxhx8Ga3FA?view)

[docker影片](https://www.youtube.com/watch?v=fqiJUltl2I0)