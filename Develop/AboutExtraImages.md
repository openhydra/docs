# 关于附加镜像

由于镜像太过庞大，我们无法将所有的镜像都打包到一个镜像中。因此，我们将一些镜像单独打包，用户可以根据自己的需求选择性的下载这些镜像。 大家可以访问这里获取 [openhydra-extra-images.tar.gz ](https://pan.baidu.com/s/1qKXHVbcGrDScBNySPuY3uA?pwd=gvzr#list/path=%2Fopenhydra%2Frelease%2Frelease-2.0)

## 加载镜像包

* 首先将这个文件复制到服务器上
* 解压并加载

```bash
# 解压这个文件
$ tar -zxvf openhydra-extra-images.tar.gz
# 循环加载 tar 文件
$ for i in $(ls *.tar); do ctr -n k8s.io i import $i; done
```