## 需求分析

根据主要的自述文件，我们目前的需求可以总结为：

1. 在 6000 的预算范围内
2. 搭建一个目前能够存储 10 TiB 数据的
3. 满足镜像站的安全和服务要求的
4. 服务器集群或单个服务器
5. 并尽可能地为以后可能的扩容或新增属性预留空间

## 需求结论

因此，我们需求的是一个对于计算性能要求较低，但需要更多的花费在存储性能上的服务器（集群）。

建议使用双机器配置：有一台冗余，避免故障的同时，可作分流。

并购置足够存储数量的硬盘，最好的情况下组成一个 RAID 阵列。

## 最终建议

在理想情况下，我们可以购买华为的 RH2288H V2 及以上的服务器，用于配置磁盘组 RAID 阵列。其支持 2 个中央处理器，二手一样稳定，[大约 ￥ 400 元人民币](https://item.taobao.com/item.htm?abbucket=10&id=615426393488&ns=1&priceTId=213e055d17406380163808976ef288&skuId=5823651283054&spm=a21n57.sem.item.3.34a47d83vpIVGw&utparam=%7B%22aplus_abtest%22%3A%2242f0a22f7063147031e9ece057c9dc28%22%7D&xxc=taobaoSearch)。

上述论证已经证明：CPU 无所谓，因此 [英特尔 ® 至强 ® 处理器 E5-2620](https://www.intel.cn/content/www/cn/zh/products/sku/64594/intel-xeon-processor-e52620-15m-cache-2-00-ghz-7-20-gts-intel-qpi/specifications.html) 已经足够。[现在二手价 ￥ 10 一颗](https://item.taobao.com/item.htm?id=773992043102&ns=1&priceTId=213e055d17406382667031585ef288&skuId=5464676258615&spm=a21n57.sem.item.46.34a47d83vpIVGw&utparam=%7B%22aplus_abtest%22%3A%22dd7ea3a306d69a02d9f36182e246bb7f%22%7D&xxc=ad_ztc)，买它两颗，正好搭上述服务器。大约 ￥ 20 元。

内存条在选择上可用性不多，上述处理器只支持 DDR3，但也足够了，买他总计 16 GiB 即可，单根 4 GiB，买它四个。[大约 ￥ 40 元人民币](https://item.taobao.com/item.htm?id=694275033514&ns=1&priceTId=2150467817406388204886533e046e&skuId=5099440478425&spm=a21n57.sem.item.98.34a47d83vpIVGw&utparam=%7B%22aplus_abtest%22%3A%22ff9c89866b211848d51a02c67e631b2b%22%7D&xxc=ad_ztc)

系统盘还是要稍微好一点的，至少得固态吧，3.5 寸 SATA 即可，128G 走起。[大约 ￥ 60 元人民币](https://item.jd.com/100028397263.html#crumb-wrap)

最后是重中之重，想要存储跟得上，SAS 硬盘得插好。[6 GiB 一个 300 块](https://item.taobao.com/item.htm?abbucket=10&id=678719109707&ns=1&priceTId=215049e917406399360532370e18b4&skuId=5889665163375&spm=a21n57.sem.item.380.34a47d83vpIVGw&utparam=%7B%22aplus_abtest%22%3A%226ebc9d82ba887734eaf7c5edab7f17de%22%7D&xxc=taobaoSearch)，四块直接 24 GiB 走起。大约 ￥ 1200 元。

综上统计：

| 物件                  | 数量 | 总计约数 |
| --------------------- | ---- | -------- |
| 华为 RH2288HV2+阵列卡 | 1    | 450      |
| 英特尔 E5-2620        | 2    | 20       |
| 4G 内存条             | 4    | 40       |
| 128G 固态硬盘         | 1    | 60       |
| 6G SAS 硬盘           | 4    | 1200     |
| 总计                  | \*   | 1770     |
