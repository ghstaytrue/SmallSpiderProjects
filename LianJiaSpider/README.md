# LianJiaSpider
## 链家爬虫
爬取天津二手房成交数据。用到python的ProcessPoolExecutor进程池。

1. 爬虫架构

   1. CrawlProcess类：配合进程池进行URL提取，并进行回调，代码中有详细介绍。
   2. ParserProcess类：配合进程池通过获取的URL爬取房子信息，对结果进行解析，返回爬取的数据。
   3. OutPutProcess类：配合进程池对上面爬取解析进程结果进行进程池处理存储。
   4. CrawlManager类：爬虫管理类，进程池负责统一管理调度爬取解析及存储进程。

2. 爬虫后续会使用代理，浏览器头进行反反爬虫。

   