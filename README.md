# Gametech情境與系統參考架構
================

*   [概述](#overview)
*   [線上真人百家樂](game1.md)
    *   [應用說明](#Game11)
    *   [架構目標](#Game12)
    *   [架構特性](#Game13)
    *   [AWS服務](#Game14)
    *   [參考架構](#Game15)
*   [老虎機](#Game2)
    *   [應用說明](#Game21)
    *   [架構目標](#Game22)
    *   [架構特性](#Game23)
    *   [AWS服務](#Game24)
    *   [參考架構](#Game25)
* * *

<h2 id="overview">概述</h2>
本文章用來說明目前坊間常見的遊戲類型，並且依照類型的應用情境、架構目標與特性、提供參考架構與相關使用的AWS服務，以供系統管理方便建構與使用。



* * *

<h2 id="Game1">線上真人百家樂</h2>
<h3 id="Game11">應用說明</h3>

線上真人百家樂是透線上直播的方式，以真人發牌方式，透過直播系統將檯面發牌資訊，即時提供遊戲玩家，以杜絕過往電腦全自動發牌或機械手臂發牌所帶來的顧忌，希望可以有更公平公正的遊戲方式。

<h3 id="Game12">架構目標</h3>

- 視訊串流為主，不能有latency 延遲
（規格一般表現在3- 5秒內）
-  需要連接多個視訊源
-   影像辨識牌
-  下注指令和現場行為要足夠流暢

<h3 id="Game13">架構特性</h3>

- 推拉RTMP, HLS, WebRTC低延遲碼流
- 影片編碼的所有基礎設施的佈建和管理都自動化，讓您在最短時間內就能部署一個簡單的視訊頻道
- 您只需為所使用的服務付費，不用前期投資編碼基礎設施
- 可靠性和彈性的項服務可管理跨多個可用區域的資源，也會自動監控其運作狀態，因此可以偵測並解決任何可能發生的問題，而不會中斷即時頻道
- 全球化網路節點與簡化的流量管理
- 加速的網路存取敏感高應用程式構特性

<h3 id="Game14">AWS服務</h3>

- [AWS Elemental MediaLive](https://aws.amazon.com/tw/medialive/)
- [AWS Elemental MediaPackage](https://aws.amazon.com/tw/mediapackage/)
- [Amazon S3](https://aws.amazon.com/tw/s3/)
- [Amazon CloudFront](https://aws.amazon.com/tw/cloudfront/)


<h3 id="Game15">參考架構</h3>

參考架構
![Alt text](Game1.jpg)


* * *

<h2 id="Game2">老虎機</h2>
<h3 id="Game21>應用說明</h3>


<h3 id="Game22>架構目標</h3>

- 前端網頁表現 Loading 很重
- 機率表現要 獨立運算
- 各個遊戲表現差異化大，機皇佔比 80%
- 
<h3 id="Game23>架構特性</h3>

- 提供超過400種的機型組合，從一般型、運算優化、到HPC高效機型，提供特定前端網頁表現與後台機率運算所需的計算力
- 依各個遊戲玩家表現，提供自動擴容與自動偵測機制，確保前端系統穩定
- 搭配CDN服務，加速老虎機前端網頁不論是圖片或是影片的內容派送

<h3 id="Game24>AWS服務</h3>

- [Amazon EC2](https://aws.amazon.com/tw/ec2/instance-types/)
- [Amazon EBS](https://aws.amazon.com/tw/ebs/volume-types/)
- [Amazon CloudFront](https://aws.amazon.com/tw/cloudfront/)


<h3 id="Game25>參考架構</h3>

參考架構
![Alt text](Game1.jpg)

* * *
