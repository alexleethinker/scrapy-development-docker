# scrapy-development-docker
Web Scraping Development Docker Container

This container includes python, selenium, beautifulsoup, scrapy, [scrapyjs] (https://github.com/scrapinghub/scrapy-splash), boto3

##Build the Image
Use docker build to buid your web scraping container

```
docker build -t scrapy .
```

##Start the Container
Use -v to mount your local development spider code

```
docker run -v ~/Documents/Development:/opt/dev -it scrapy  /bin/bash
```

##附件说明
我在原来Dockerfile的基础上修改了  
1. Ubuntu源设置为阿里云，加快国内访问速度  
2. Ubuntu使用了14.04版本号，避免默认采用latest（如果你本地的docker已经安装了Ubuntu 14.04的镜像的话会节省很多时间）
