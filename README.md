# FastDFS-Nginx Docker 

[fastdfs](https://github.com/happyfish100/fastdfs)

Usage:

```
docker run -dti --network=host --name tracker -v /var/fdfs/tracker:/var/fdfs ygqygq2/fastdfs-nginx tracker

docker run -dti --network=host --name storage0 -e TRACKER_SERVER=10.1.5.85:22122 -v /var/fdfs/storage0:/var/fdfs ygqygq2/fastdfs-nginx storage

docker run -dti --network=host --name storage1 -e TRACKER_SERVER=10.1.5.85:22122 -v /var/fdfs/storage1:/var/fdfs ygqygq2/fastdfs-nginx storage

docker run -dti --network=host --name storage2 -e TRACKER_SERVER=10.1.5.85:22122 -e GROUP_NAME=group2 -e PORT=22222 -v /var/fdfs/storage2:/var/fdfs ygqygq2/fastdfs-nginx storage
```
1.处理文件名，保持上传的文件名称与下载的文件名称一致；   
2.自定义404页面