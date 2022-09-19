## 使用方法：

```
sudo cp ./weave /usr/local/bin/
sudo chmod a+x /usr/local/bin/weave
# 初始化weave 网络插件,在$host1上
weave launch 

# 初始化weave 网络插件,在$host2上
weave launch $host1

# 创建容器box1,在$host1上
eval $(weave env)
docker run -itd --name box1 --rm busybox

# 创建容器box2,在$host2上
eval $(weave env)
docker run -itd --name box1 --rm busybox

# 此时两个容器间，可以使用ping box1/box2进行连接了

```
