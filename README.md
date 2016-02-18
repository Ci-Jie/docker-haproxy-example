## Docker-HAProxy-Example

### 簡介
此範例是將 HAProxy 建置在 docker container 上，透過 docker compose 將範例 web 對應到 8080 與 8081 port 並與 HAProxy 串接，當使用者重新整理瀏覽器時，系統會以預設的演算法 - round robin 將 request 循序導到兩個 web ，實現負載平衡(load balance)。 

### 前置安裝：

透過執行 install.sh 安裝 docker 與 docker-compose：

```
./install.sh
```

安裝完成後，使用下列查詢指令觀看版本並且驗證是否安裝成功：

```
docker --version ; docker-compose --version

#結果:
Docker version 1.10.1, build 9e83765
docker-compose version 1.6.0, build d99cad6
```

接下來，執行 docker-compose.yml 安裝範例，指令如下：

```
sudo docker-compose up
```

開啟瀏覽器，輸入 ip 可以檢視結果。
