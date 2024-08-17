# MinerU docker image

容器默认工作路径

镜像默认为cpu模式，不安装nividia等驱动

## Run

1. 构建 Docker 镜像

	```shell
	docker build -t mineru-env .
	```

2.  运行 Docker 容器

   ```shell
   # docker run --gpus all -it mineru-env # 启用gpu
   docker run -it mineru-env # 不启用gpu（默认）
   ```

3. 容器启动后测试从仓库中下载样本文件，并测试（optional）

   ```shell
   # wget https://gitee.com/myhloli/MinerU/raw/master/demo/small_ocr.pdf
   magic-pdf -p small_ocr.pdf
   ```
