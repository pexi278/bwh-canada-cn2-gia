# 搬瓦工加拿大套餐：温哥华CN2 GIA机房怎么选，CN2 GIA-E价格、配置与购买优惠一次说清

搜“搬瓦工加拿大套餐”的人，诉求一般很明确：想要一个北美节点，又不想牺牲国内访问质量。这篇文章先把最关键的事说清楚——搬瓦工（BandwagonHost）在加拿大只有温哥华两个机房，其中 CABC_6 接入 CN2 GIA 线路，但它不能单独购买，只能通过特定套餐迁移过去。哪些套餐能用加拿大机房、价格多少、实测表现如何、有没有能用的优惠码，下面一次讲完。

## 先说结论：加拿大机房怎么买

搬瓦工目前在加拿大温哥华有两个机房：

- **CABC_1**：普通线路机房，Basic 系列（KVM 套餐）可以直接选择，价格从 $49.99/年起。
- **CABC_6**：CN2 GIA 线路机房，三网回程走 CN2 GIA，只有 CN2 GIA-E（E-Commerce）系列套餐能用，购买后可以在 KiwiVM 后台免费迁移过去，数据不丢。

所以严格来说，搬瓦工没有叫“加拿大套餐”的独立产品。想用温哥华 CN2 GIA，买 CN2 GIA-E 套餐再迁移机房就行，入门款季付 $49.99、年付 $169.99。另外 THE PLAN v2 这类限量版套餐的可选机房里也包含加拿大温哥华 CN2 GIA，碰到补货也可以考虑。

👉 [查看支持温哥华 CN2 GIA 的 CN2 GIA-E 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=87)

## CABC_1 和 CABC_6 的区别在哪

两个机房都在温哥华，硬件也一样，区别主要在线路。

CABC_1 走普通线路，价格便宜，Basic 系列年付 $49.99 起就能用，但国内访问质量一般，晚高峰容易波动。它更适合做面向北美本地用户的服务，比如面向加拿大用户的网站、欧美方向的代理节点。

CABC_6 接入 CN2 GIA（电信）、CMIN2（移动）和 CUP（联通精品）线路，回程全程走电信 CN2 骨干（59.43.x.x 段），这是搬瓦工线路体系里最高端的一档。实测数据显示，温哥华到国内三网的延迟大致在 140-200ms，和洛杉矶 CN2 GIA 机房处于同一水平线，晚高峰丢包控制得不错。

2025 年年中，官方把 CABC_1 和 CABC_6 都做了硬件升级：CPU 换成 AMD EPYC（Genoa），硬盘换成 NVMe SSD。从第三方跑分看，CABC_6 的机器 Geekbench 6 单核 1803 分左右，磁盘 4K 读写超过 300MB/s，机房出口实测能跑到数 Gbps。这个硬件水平在 $169.99/年价位的 VPS 里算是相当能打的。

> 提示：CABC_6 不是所有套餐都能用。能不能选或迁移，以 KiwiVM 控制面板里显示的机房列表为准。

## 哪些套餐可以用加拿大机房

按搬瓦工当前的套餐体系（Basic、E-Commerce、SLA、Ultra 四大系列），加拿大机房的可用情况如下：

- **Basic（KVM）系列**：可选 CABC_1（普通线路），不可用 CABC_6。
- **CN2 GIA-E（E-Commerce）系列**：可选 CABC_6（CN2 GIA），也可迁移到 CABC_1。
- **SLA 系列**：固定洛杉矶 DC5 机房，不支持加拿大。
- **Ultra 系列**（香港/东京/大阪/新加坡）：机房固定，不支持加拿大。
- **迪拜 E-Commerce 系列**：默认迪拜机房，迁移列表里有 CABC_1，但没有 CABC_6。
- **限量版套餐**（如 THE PLAN v2，$119/年）：可选机房覆盖加拿大温哥华 CN2 GIA，限量发售，售罄后需等补货。

如果你就是冲着加拿大 CN2 GIA 来的，CN2 GIA-E 系列是唯一常规入口。

## 搬瓦工全套餐价格对比（当前官网在售全部方案）

以下价格均来自官网当前公开页面，币种为美元。购买链接基于 AFF 参数生成，指向对应套餐页面。

### Basic 系列（可选温哥华 CABC_1 普通线路）

| 套餐 | 配置（CPU/内存/SSD） | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| Basic 20G | 2核 / 1GB / 20GB | 1TB/月，1Gbps | $49.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=44) |
| Basic 40G | 3核 / 2GB / 40GB | 2TB/月，1Gbps | $52.99/半年、$99.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=45) |
| Basic 80G | 4核 / 4GB / 80GB | 3TB/月，1Gbps | $19.99/月、$199.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=46) |
| Basic 160G | 5核 / 8GB / 160GB | 4TB/月，1Gbps | $39.99/月、$399.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=47) |
| Basic 320G | 6核 / 16GB / 320GB | 5TB/月，1Gbps | $79.99/月、$799.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=48) |
| Basic 480G | 7核 / 24GB / 480GB | 6TB/月，1Gbps | $119.99/月、$1199.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=49) |

### CN2 GIA-E 系列（可选温哥华 CABC_6 CN2 GIA）

| 套餐 | 配置（CPU/内存/SSD） | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| CN2 GIA-E 20G | 2核 / 1GB / 20GB | 1TB/月，2.5Gbps | $49.99/季、$169.99/年 | [ 购买入门款](https://bandwagonhost.com/aff.php?aff=79616&pid=87) |
| CN2 GIA-E 40G | 3核 / 2GB / 40GB | 2TB/月，2.5Gbps | $89.99/季、$299.99/年 | [ 购买40G](https://bandwagonhost.com/aff.php?aff=79616&pid=88) |
| CN2 GIA-E 80G | 4核 / 4GB / 80GB | 3TB/月，2.5Gbps | $56.99/月、$549.99/年 | [ 购买80G](https://bandwagonhost.com/aff.php?aff=79616&pid=89) |
| CN2 GIA-E 160G | 6核 / 8GB / 160GB | 5TB/月，5Gbps | $86.99/季、$879.99/年 | [ 购买160G](https://bandwagonhost.com/aff.php?aff=79616&pid=90) |
| CN2 GIA-E 320G | 8核 / 16GB / 320GB | 8TB/月，5Gbps | $159.99/季、$1599.99/年 | [ 购买320G](https://bandwagonhost.com/aff.php?aff=79616&pid=91) |
| CN2 GIA-E 640G | 10核 / 32GB / 640GB | 10TB/月，10Gbps | $289.99/季、$2759.99/年 | [ 购买640G](https://bandwagonhost.com/aff.php?aff=79616&pid=92) |
| CN2 GIA-E 1280G | 12核 / 64GB / 1280GB | 12TB/月，10Gbps | $549.99/季、$5399.99/年 | [ 购买1280G](https://bandwagonhost.com/aff.php?aff=79616&pid=93) |
| CN2 GIA-E 1280G 大流量15T | 12核 / 64GB / 1280GB | 15TB/月，10Gbps | $679/月、$6790/年 | [ 查看大流量版](https://bandwagonhost.com/aff.php?aff=79616&pid=160) |
| CN2 GIA-E 1280G 大流量20T | 12核 / 64GB / 1280GB | 20TB/月，10Gbps | $899/月、$8999/年 | [ 查看大流量版](https://bandwagonhost.com/aff.php?aff=79616&pid=161) |
| CN2 GIA-E 1280G HICPU | 24核 / 64GB / 1280GB | 12TB/月，10Gbps | $749.99/季、$7599/年 | [ 查看高CPU版](https://bandwagonhost.com/aff.php?aff=79616&pid=148) |

### SLA 系列（固定洛杉矶，99.99% SLA 保障）

| 套餐 | 配置（CPU/内存/NVMe） | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| SLA 20G | 2核 / 1GB / 20GB | 1TB/月，2.5Gbps | $65.89/季、$239.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=164) |
| SLA 40G | 3核 / 2GB / 40GB | 2TB/月，2.5Gbps | $116.99/季、$399.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=165) |
| SLA 80G | 4核 / 4GB / 80GB | 3TB/月，2.5Gbps | $69.99/月、$699.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=166) |
| SLA 160G | 6核 / 8GB / 160GB | 5TB/月，5Gbps | $109.99/月、$1099.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=167) |
| SLA 320G | 8核 / 16GB / 320GB | 8TB/月，5Gbps | $199.99/月、$1999.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=168) |
| SLA 640G | 10核 / 32GB / 640GB | 10TB/月，10Gbps | $369.99/月、$3699.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=169) |
| SLA 1280G | 12核 / 64GB / 1280GB | 12TB/月，10Gbps | $699.99/月、$6999.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=170) |
| SLA 1280G 大流量15T | 12核 / 64GB / 1280GB | 15TB/月，10Gbps | $879.99/月、$8799.99/年 | [ 查看大流量版](https://bandwagonhost.com/aff.php?aff=79616&pid=171) |
| SLA 1280G 大流量20T | 12核 / 64GB / 1280GB | 20TB/月，10Gbps | $1159.99/月、$11598.99/年 | [ 查看大流量版](https://bandwagonhost.com/aff.php?aff=79616&pid=172) |

### Ultra 系列 · 香港 CN2 GIA（机房固定）

| 套餐 | 配置 | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| 香港 40G | 2核 / 2GB / 40GB | 500GB/月，1Gbps | $89.99/月、$899.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=95) |
| 香港 80G | 4核 / 4GB / 80GB | 1TB/月，1Gbps | $155.99/月、$1559.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=96) |
| 香港 160G | 6核 / 8GB / 160GB | 2TB/月，1Gbps | $299.99/月、$2999.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=97) |
| 香港 320G | 8核 / 16GB / 320GB | 4TB/月，1Gbps | $589.99/月、$5899.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=98) |
| 香港 640G | 10核 / 32GB / 640GB | 6TB/月，1Gbps | $989.99/月、$9989.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=122) |
| 香港 1280G | 12核 / 64GB / 1280GB | 8TB/月，1Gbps | $1889.99/月、$18989.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=124) |

### Ultra 系列 · 大阪 CN2 GIA（机房固定）

| 套餐 | 配置 | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| 大阪 40G | 2核 / 2GB / 40GB | 500GB/月，1.5Gbps | $49.99/月、$499.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=134) |
| 大阪 80G | 4核 / 4GB / 80GB | 1TB/月，1.5Gbps | $86.99/月、$869.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=135) |
| 大阪 160G | 6核 / 8GB / 160GB | 2TB/月，1.5Gbps | $165.99/月、$1665.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=136) |
| 大阪 320G | 8核 / 16GB / 320GB | 4TB/月，1.5Gbps | $329.99/月、$3279.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=137) |
| 大阪 640G | 10核 / 32GB / 640GB | 6TB/月，1.5Gbps | $549.99/月、$5549.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=138) |
| 大阪 1280G | 12核 / 64GB / 1280GB | 8TB/月，1.5Gbps | $1059.99/月、$10559.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=139) |

### Ultra 系列 · 东京 CN2 GIA（机房固定）

| 套餐 | 配置 | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| 东京 40G | 2核 / 2GB / 40GB | 500GB/月，1.2Gbps | $89.99/月、$899.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=108) |
| 东京 80G | 4核 / 4GB / 80GB | 1TB/月，1.2Gbps | $155.99/月、$1559.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=109) |
| 东京 160G | 6核 / 8GB / 160GB | 2TB/月，1.2Gbps | $299.99/月、$2999.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=110) |
| 东京 320G | 8核 / 16GB / 320GB | 4TB/月，1.2Gbps | $589.99/月、$5899.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=111) |
| 东京 640G | 10核 / 32GB / 640GB | 6TB/月，1.2Gbps | $989.99/月、$9989.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=123) |
| 东京 1280G | 12核 / 64GB / 1280GB | 8TB/月，1.2Gbps | $1889.99/月、$18989.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=125) |

### Ultra 系列 · 新加坡 CN2 GIA（机房固定）

| 套餐 | 配置 | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| 新加坡 40G | 2核 / 2GB / 40GB | 500GB/月，1.5Gbps | $49.99/月、$499.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=173) |
| 新加坡 80G | 4核 / 4GB / 80GB | 1TB/月，1.5Gbps | $86.99/月、$869.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=174) |
| 新加坡 160G | 6核 / 8GB / 160GB | 2TB/月，2.5Gbps | $165.99/月、$1665.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=175) |
| 新加坡 320G | 8核 / 16GB / 320GB | 4TB/月，2.5Gbps | $329.99/月、$3199/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=176) |
| 新加坡 640G | 10核 / 32GB / 640GB | 6TB/月，5Gbps | $549.99/月、$5549.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=177) |
| 新加坡 1280G | 12核 / 64GB / 1280GB | 8TB/月，5Gbps | $1059.99/月、$10559.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=178) |

### 迪拜 E-Commerce 系列（默认迪拜，可迁移至 CABC_1）

| 套餐 | 配置 | 流量/带宽 | 价格 | 购买 |
| --- | --- | --- | --- | --- |
| 迪拜 20G | 2核 / 1GB / 20GB | 500GB/月，1Gbps | $19.99/月、$169.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=114) |
| 迪拜 40G | 3核 / 2GB / 40GB | 1TB/月，1Gbps | $32.99/月、$299.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=115) |
| 迪拜 80G | 4核 / 4GB / 80GB | 2TB/月，1Gbps | $56.99/月、$549.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=116) |
| 迪拜 160G | 6核 / 8GB / 160GB | 3TB/月，1Gbps | $86.99/月、$879.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=117) |
| 迪拜 320G | 8核 / 16GB / 320GB | 4TB/月，1Gbps | $159.99/月、$1599.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=118) |
| 迪拜 640G | 10核 / 32GB / 640GB | 5TB/月，1Gbps | $289.99/月、$2759.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=119) |
| 迪拜 1280G | 12核 / 64GB / 1280GB | 6TB/月，1Gbps | $549.99/月、$5399.99/年 | [ 查看套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=120) |

简单概括这张表：想用温哥华 CN2 GIA，从 CN2 GIA-E 系列 $169.99/年那档进；只需要加拿大普通线路，Basic 系列 $49.99/年就够；需要香港、日本、新加坡的极致对华线路，选对应 Ultra 套餐，但这些套餐不能迁移到加拿大。

👉 [浏览全部在售套餐和最新价格](https://bit.ly/BandwagonHost)

## 优惠码与付款方式

搬瓦工的优惠体系比较简单，主要是循环折扣码，对月付、季付、年付都生效，续费同样可用。目前多个更新到近期的优惠信息源列出的可用码是 **BWHCGLUKKB**，循环折扣约 6.77%——以 CN2 GIA-E 年付 $169.99 计算，能省 $11 左右。需要留意的是，2025 年双十一前后曾有一批老优惠码集中失效的记录，所以结账时以优惠码输入框的实际抵扣结果为准，码失效就按原价买，搬瓦工热门套餐长期缺货，等折扣的意义通常不大。

付款支持支付宝、PayPal 和信用卡，注册和购买流程对国内用户友好。常规套餐新购后有 30 天退款窗口，不满意可以申请退回。

## 购买后怎么把机器迁到温哥华

流程不复杂，全部在 KiwiVM 控制面板完成：

1. 购买 CN2 GIA-E 套餐（或其他包含加拿大机房的可选套餐）。
2. 登录 KiwiVM 面板，在机房迁移（Migrate）选项里找到温哥华机房：普通线路对应 CABC_1，CN2 GIA 对应 CABC_6。
3. 确认迁移，系统自动搬移数据，IP 会更换，数据不丢失。
4. 迁移完成后可以用 BestTrace 之类工具验证回程路由，CABC_6 的回程应该能看到 59.43 开头的 CN2 骨干节点。

一个务实的建议：迁移前先在面板里记下旧 IP 的 rDNS 设置，换 IP 后重新配置一下。另外 CABC_6 偶尔会出现资源紧张导致的暂时无法迁入，遇到这种情况过几天再试即可。

## 常见问题

**温哥华 CN2 GIA 和洛杉矶 DC6/DC9 怎么选？**

两条线路都是 CN2 GIA，国内延迟都在 140-180ms 区间，日常使用差别不大。洛杉矶机房库存更充足、可选套餐更多；温哥华的优势是地理位置偏西北，到加拿大本地和美西北的网络质量更好，如果你人在加拿大或主要服务北美西海岸用户，温哥华更合适。纯从性价比看，CN2 GIA-E 系列两条线路价格完全一样，买了之后随时可以互迁，先选哪个都不亏。

**加拿大套餐需要单独购买吗？**

不需要。CABC_6 是 CN2 GIA-E 套餐的可选机房，买套餐后后台迁移即可，不收迁移费。

**流量超了怎么办？**

超出月流量后机器不会停，但带宽会被限制到较低速率，次月恢复。CN2 GIA-E 入门款 1TB/月对轻度使用足够，跑大流量业务建议上 40G 及以上档位。

**支持 IPv6 吗？**

CN2 GIA-E 套餐提供 routed /64 的 IPv6 子网，面板里可以查看分配地址。迪拜系列目前不支持 IPv6，这是官方页面明确标注的。

搬瓦工加拿大套餐的核心信息就是这些：两个机房、一条 CN2 GIA 线路、一个入门价 $169.99/年的 CN2 GIA-E 套餐。硬件刚升级过，回程线路是搬瓦工体系里的顶级配置，如果你需要一个既在北美、国内访问又稳定的节点，这套方案值得列入备选。

👉 [前往官网选择 CN2 GIA-E 套餐并迁移温哥华机房](https://bandwagonhost.com/aff.php?aff=79616&pid=87)
