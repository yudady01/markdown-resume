<center>
    <h1>林炫羽</h1>
    <div>          
        <span>應徵職缺：</span>
        <span>軟體開發工程師</span>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
        <span>工作經驗：</span>
        <span>15 年</span>  
    </div>
    <div>
        <span>
            <img src="assets/phone-solid.svg" width="14px">
            0933-178-841
        </span>
        &nbsp;
        <span>
            <img src="assets/mail-filled-svgrepo-com.svg" width="16px">
            yudady@gmail.com
        </span>
        &nbsp;
        <span>
            <img src="assets/man-and-woman-avatar-svgrepo-com.svg" width="18px">
            男
        </span>
        &nbsp;
        <span>
            <img src="assets/graduation-cap-solid.svg" width="18px">
            靜宜大學碩士
        </span>
    </div>
</center>

## <img src="assets/tools-solid.svg" width="30px"> 技能清單

- 基礎知識：多年一線java開發經驗，具備良好的編碼能力，具備良好的麵向對象的編程思想，對並發編程，對鎖機製，線程池都有深入理解。
- 框架：對Spring、SpringBoot、SpringData、MyBatis，多年實戰經驗，可以按照需求快讀構建項目，閱讀過Spring核心源碼。
- 微服務：對Dockerfile、k8s yaml處理，有線上項目經驗。
- 數據庫：對Mysql與Oracle有多年實戰經驗，處理索引的優化及plsql編寫有實際的開發經驗。
- 中間件：Redis多數據類型緩存應用，Kafka訊息不丟和重復，消費以及消息投遞一致性問題，有實際的項目經驗。
- 熟悉大型網站高並發設計方案：對nginx、cdn、dns、https等都有深入的理解。
- 前端技術：Angular、Vue、webpack、JQuery、Bootstrap，有實際的項目經驗。
- GitOps：Jenkins、Maven、Gradle、ELK、GCP、Terraform，有實際的項目經驗。

## <img src="assets/project-diagram-solid.svg" width="30px"> 項目經歷

### 優訊軟體：支付匹配系統（ubPay項目）

* **項目描述**：
    - 起因：因銀行卡取得困難且三方支付渠道短缺且收費高
    - 功能：集團內部充值用戶往提現用戶銀行卡充值，充值完成後截圖下提交給審核員處理

* **項目架構**：
    - 技術：
        - 在GCP平台上用Terraform構建k8s系統，使用Jenkins構建image部屬應用服務
        - Redis、Mysql、Kafka、ElasticSearch、Kibana、core-ng(類Spring框架,https://github.com/neowu/core-ng-project)
    - 功能描述：
        - 撰寫後台管理系統，參與產品架構設計、開發、維護、除錯處理
        - 網站的前後端及相關API 開發與串接
        - 以API模式接入vander提交的資料，進行集團內部支付匹配
        - 首先需要有提現用戶發起固定金額提現(100 200 300 ..)，把提現金額存入提現池，當另外一個用戶發起充值，從提現池找出可用金額返回給用戶選擇金額
        - 充值用戶先選擇充值金額（提現池裡面的金額），選定金額後返回提現用戶的銀行卡資訊，當用戶充值完成後，需要上傳充值截圖，審核員確認資料無誤後執行回調API，即充值提現完成
        - 此項目用Terraform + k8s構建在GCP平台上，使用Jenkins部屬不停機服務，上版需要做到向下兼容
        - 用Saga分散式模式以Kafka事件驅動對業務流程的狀態更新，用Redis進行緩存數據

### 格拉墨

* **項目描述**：
    - 起因：因銀行卡取得困難且三方支付渠道短缺且收費高
    - 功能：集團內部充值用戶往提現用戶銀行卡充值，充值完成後截圖下提交給審核員處理

* **項目架構**：
    - 技術：
        - redis、postgresql、mongodb、rabbitmq、docker
    - 功能描述：
        - 撰寫後台管理系統，參與產品架構設計、開發、維護、除錯處理

### 優訊軟體：包網平台（pf2項目）

* **項目描述**：
    - 包網平台:體育/真人/棋牌/老虎機/彩票

* **項目架構**：
    - 技術：
        - SpringBoot、Spring data jpa、core-ng(類Spring框架)
        - WebLogic、Jersey JAX-RS、JBPM、Quartz Scheduler、Hibernate、Querydsl、JasperReport、PLSQL
        - Oracle、Redis、Kafka、Nginx、Prometheus、Grafana
        - webpack、Angular、React
    - 功能描述：
        - 前台使用React與後台使用Angular，採前後分離，API經Nginx反向代理處理
        - 玩家與代理管理：資金記錄、層級設置、返水系統，交易紀錄、流水控制、代理資料、佣金計算
        - VIP里程碑：彩票投注里程、综合投注里程、生日禮金、節日禮金、福利派發、會員等級
        - 訊息：站內信息、公告管理、郵件、簡訊
        - 活動：活動工具、每日登入送、充值送、紅包送 活動舉辦、權限控管、廣告、推廣連結
        - 三方遊戲：接入pt、mgs、ttg、saba、ky、ag等廠商遊戲
        - 支付金流：（支付寶、微信、QQ掃碼、線上充提...）審核功能、歷史查詢（記錄玩家每筆存款歷史），提現自動審核，信用分類
        - 團隊管理、賬號管理、部門系統、權限設置、代理報表
        - 早期使用EJB開發，近年把功能拆分模組化再加上API優化往微服務架構轉移，使用Jenkins部屬不停機服務，上版需要做到向下兼容
        - 使用Quartz Scheduler處理job定時功能

### 艾米科技：支付聚合系統

* **項目描述**：
    - 通用聚合支付平台，提供已串接完成的第3方支付系統，與自動上分系統，部屬在GCP上的平台，供客戶開箱即用

* **項目架構**：
    - 技術：vue、jquery、bootstrap、websocket / redis、oracle、jsoup、elk / zabbix、jenkins
    - 功能描述：
        - 渠道管理:接入渠道API通道
        - 商家管理:對商家的基本信息管理
        - 訂單管理:用戶通過渠道支付成功，渠道把交易訂單送到聚合系統，聚合系統再上送給商戶

## <img src="assets/briefcase-solid.svg" width="30px"> 工作經歷

| 在職時間            | 公司   | 職務    | 項目內容         |
|:----------------|:-----|:------|:-------------|
| 2023/02~        | 格拉墨  | 資深工程師 | 三方遊戲平台       |
| 2019/02~2022/12 | 優訊軟體 | 開發組長  | 包網平台         |
| 2016/11~2018/11 | 艾米科技 | 資深工程師 | 支付聚合系統       |
| 2013/04~2016/11 | 豐揚科技 | 高級工程師 | 電信業系統，手機庫存維修 |
| 2011/06~2013/04 | 億力資訊 | 高級工程師 | 財政部財稅案       |
| 2009/05~2011/06 | 緯創軟體 | 工程師   | 萬海航運(船運系統開發) |
| 2005/03~2009/03 | 創世紀  | 工程師   | 門戶網站         |


