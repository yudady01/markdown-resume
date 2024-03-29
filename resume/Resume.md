<center>
    <h1>林炫羽</h1>
    <div>
        <span>
            <img src="assets/graduation-cap-solid.svg" width="18px">
            靜宜大學應用化學系碩士(1997-2000)&nbsp;&nbsp;靜宜大學應用化學系學士(1997-1993)
        </span>
    </div>
    <div>
        <span>
            <img src="assets/phone-solid.svg" width="14px">
            0933-178-841
        </span>
        &nbsp;&nbsp;&nbsp;&nbsp;
        <span>
            <img src="assets/mail-filled-svgrepo-com.svg" width="16px">
            yudady@gmail.com
        </span>
        &nbsp;&nbsp;&nbsp;&nbsp;
        <span>
            <img src="assets/man-and-woman-avatar-svgrepo-com.svg" width="18px">
            男
        </span>
        &nbsp;&nbsp;&nbsp;&nbsp;
        <span><img src="assets/coding-browser-svgrepo-com.svg" width="18px"></span>
        <span>16 年</span>
    </div>
</center>

## <img src="assets/briefcase-solid.svg" width="30px"> 工作經歷

| 在職時間            | 公司   | 職務    | 項目內容         |
|:----------------|:-----|:------|:-------------|
| 2023/02~至今      | 葛拉墨  | 資深工程師 | 三方遊戲平台       |
| 2019/02~2022/12 | 優訊軟體 | 開發組長  | 三方遊戲平台與彩票系統  |
| 2018/11~2019/02 | 聚力國際 | 資深工程師 | 體育數據整合系統     |
| 2016/11~2018/11 | 艾米科技 | 資深工程師 | 支付聚合系統       |
| 2013/04~2016/11 | 豐揚科技 | 高級工程師 | 電信業系統，手機庫存維修 |
| 2011/06~2013/04 | 億力資訊 | 高級工程師 | 財政部財稅案       |
| 2009/05~2011/06 | 緯創軟體 | 工程師   | 萬海航運(船運系統開發) |
| 2005/03~2009/03 | 創世紀  | 工程師   | 門戶網站         |

## <img src="assets/tools-solid.svg" width="30px"> 技能清單

- 基礎知識：多年一線開發經驗，具備良好的編碼能力，具備良好的麵向對象的編程思想，對並發編程，對鎖機製，線程池都有深入理解。
- 框架：對Spring、SpringBoot、SpringData、MyBatis，多年實戰經驗，可以按照需求快讀構建項目，閱讀過Spring核心源碼。
- 微服務：對Dockerfile、k8s yaml處理，有線上項目經驗。
- 數據庫：對Mysqlg、postgresqlg、Oracle有多年實戰經驗，處理索引的優化及plsql編寫有實際的開發經驗。
- 中間件：Redis，了解底層磁盤及網絡IO模型，數據持久化機製，多數據類型緩存應用有實際的經驗。Kafka、rabbitmq，訊息不丟和重復，消費以及消息投遞一致性問題，有實際的項目經驗。
- 熟悉大型網站高並發設計方案：對nginx、cdn、dns、https等都有深入的理解。
- 前端技術：Angular、Vue、webpack、JQuery、Bootstrap，有實際的項目經驗。
- GitOps：Jenkins、Maven、Gradle、ELK、GCP、Terraform、Prometheus、Grafana，有實際的項目經驗。

## <img src="assets/project-diagram-solid.svg" width="30px"> 項目經歷

### 葛拉墨

* **項目描述**：
    - 整合三方遊戲，提供客戶與代理分成系統

* **項目架構**：
    - 技術：
        - Redis、mongoDB、postgresql 、rabbitmq、ElasticSearch、Kibana
    - 項目描述：
        - 串接三方遊戲平台模組
        - 充值提現商戶模組
        - 客戶與代理模組
        - 活動模組
        - 訊息模組

### 優訊軟體：支付匹配系統（ubPay項目）

* **項目描述**：
    - 起因：因銀行卡取得困難且三方支付渠道短缺且收費高
    - 功能：集團內部充值用戶往提現用戶銀行卡充值，充值完成後截圖下提交給審核員處理

* **項目架構**：
    - 技術：
        - 在GCP平台上用Terraform構建k8s系統，使用Jenkins構建image部屬應用服務
        - Redis、Mysql、Kafka、ElasticSearch、Kibana、core-ng(類Spring框架,https://github.com/neowu/core-ng-project)
    - 模塊：vander（廠商資訊，白名單，api回調網址），充值提現（廠商提交過來的充值提現資訊），審核員操作功能
    - 項目描述：
        - 以API模式接入vander提交的資料，進行集團內部支付匹配
        - 首先需要有提現用戶發起固定金額提現(100 200 300 ..)，把提現金額存入提現池，當另外一個用戶發起充值，從提現池找出可用金額返回給用戶選擇金額
        - 充值用戶先選擇充值金額（提現池裡面的金額），選定金額後返回提現用戶的銀行卡資訊，當用戶充值完成後，需要上傳充值截圖，審核員確認資料無誤後執行回調API，即充值提現完成
        - 此項目用Terraform + k8s構建在GCP平台上，使用Jenkins部屬不停機服務，上版需要做到向下兼容
        - 用Kafka執行事件驅動模式開發，業務流程的狀態更新，用Redis進行緩存數據

### 優訊軟體：遊戲平台（pf2項目）

* **項目描述**：
    - 遊戲項目：三方遊戲平台接入與彩票系統

* **項目架構**：
    - 技術：
        - SpringBoot、Spring data jpa、core-ng(類Spring框架)
        - Weblogic、Jersey JAX-RS、JBPM、Quartz Scheduler、Hibernate、Querydsl、JasperReport、PLSQL
        - Oracle、Redis、Kafka、Prometheus、Grafana
        - Angular、webpack、React
    - 模塊：帳號、註冊與推廣連接、活動、返點、三方遊戲接入、支付、里程碑、獎池、訊息推送、郵件、簡訊、訂單、任務排程、報表、公告、彩票
    - 項目描述：
        - 前台使用React與後台Angular，API經Nginx反向代理
        - 註冊：會員、代理
        - 會員組：會員等級與信用分類
        - VIP里程碑：彩票投注里程、综合投注里程、生日禮金、節日禮金、福利派發
        - 訊息：站內信息、公告管理、郵件、簡訊
        - 活動：活動工具、每日登入送、充值送、紅包送
        - 三方遊戲：接入pt、mgs、ttg、saba、ky、ag等廠商遊戲
        - 支付；充值提現，提現自動審核
        - 早期使用EJB開發，近年把功能拆分模組化再加上API優化往微服務架構轉移，使用Jenkins部屬不停機服務，上版需要做到向下兼容
        - 使用Quartz Scheduler處理job定時功能

### 聚力國際：體育資料整合

- 體育數據清洗系統:整理購買來的即時數據
- 使用技術：thymeleaf、jquery / springboot、mybatis、mysql、ElasticSearch、Apache Storm

### 艾米科技：支付聚合系統

- 通用聚合支付平台，提供已串接完成的第3方支付系統，與自動上分系統，部屬在GCP上的平台，供客戶開箱即用
- 使用技術：vue、jquery、bootstrap、websocket / redis、oracle、jsoup、elk / zabbix、jenkins

