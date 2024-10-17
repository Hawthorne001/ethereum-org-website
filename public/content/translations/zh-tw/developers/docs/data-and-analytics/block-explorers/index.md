---
title: 區塊瀏覽器
description: 區塊瀏覽器簡介，這是你進入區塊鏈資料世界的入口，在這裡你可以查詢有關交易、帳戶、合約等資訊。
lang: zh-tw
sidebarDepth: 3
---

區塊瀏覽器是你存取以太坊資料的入口。 你可以使用區塊瀏覽器來查看區塊、交易、驗證者、帳戶及其他鏈上活動的即時資料。

## 基本資訊 {#prerequisites}

你應該瞭解以太坊的基本概念，以便能夠理解區塊瀏覽器提供的資料。 推薦你從[以太坊簡介](/developers/docs/intro-to-ethereum/)開始。

## 服務 {#services}

- [Etherscan](https://etherscan.io/) -_ 也提供中文、韓文、俄文及日文版_
- [3xpl](https://3xpl.com/ethereum)
- [Beaconcha.in](https://beaconcha.in/)
- [Blockchair](https://blockchair.com/ethereum) -_也提供西班牙文、法文、義大利文、荷蘭文、葡萄牙文、俄文、中文及波斯文版_
- [Blockscout](https://eth.blockscout.com/)
- [Chainlens](https://www.chainlens.com/)
- [DexGuru Block Explorer](https://ethereum.dex.guru/)
- [Etherchain](https://www.etherchain.org/)
- [Ethernow](https://www.ethernow.xyz/)
- [Ethplorer](https://ethplorer.io/) -_ 也提供中文、西班牙文、法文、土耳其文、俄文、韓文及越南文版_
- [EthVM](https://www.ethvm.com/)
- [OKLink](https://www.oklink.com/eth)
- [Rantom](https://rantom.app/)

## 開源工具 {#open-source-tools}

- [Otterscan](https://otterscan.io/)
- [lazy-etherscan](https://github.com/woxjro/lazy-etherscan)

## 數據資料 {#data}

以太坊的設計是透明的，因此一切都是可驗證的。 區塊瀏覽器提供了獲取此資訊的介面。 如果你需要這些資料，這適用於以太坊主網和測試網。 資料被分為執行資料和共識資料。 執行資料指的是特定區塊中已被執行的交易。 共識資料指的是區塊本身及提出區塊的驗證者。

以下是可以從區塊瀏覽器取得的資料類型的摘要。

### 執行資料 {#execution-data}

新區塊每 12 秒會添加到以太坊上（除非區塊提議者漏掉了其提議輪次），因此接近恆定的資料流被加到區塊瀏覽器上。 區塊包含許多你可能覺得有用的重要資料：

**標準資料**

- 區塊高度 - 目前區塊建立時，區塊的編號及區塊鏈的長度（以區塊為單位）
- 時間戳 - 區塊被提議的時間
- 交易 - 被打包進區塊的交易數量
- 費用接收者 - 從交易中收到燃料費與小費的地址
- 區塊獎勵 - 提出區塊的驗證者獲得的以太幣數量
- 大小 - 區塊中的資料大小（以位元組計算）
- 消耗的燃料 - 區塊中交易消耗的燃料單位總數
- 燃料限制 - 區塊中交易設定的總燃料限制
- 每單位燃料的基本費用 - 讓交易能夠打包進區塊所需的最低乘數
- 銷毀費用 - 區塊中銷毀的以太幣數量
- 額外資料 - 任何建置者加進區塊的額外資料

**進階資料**

- 雜湊 - 代表區塊頭（區塊的唯一識別碼）的密碼學雜湊。
- 父雜湊 - 目前區塊之前區塊的雜湊
- StateRoot - 默克爾樹的根雜湊，存儲了整個系統的狀態

### Gas費 {#gas}

區塊瀏覽器不僅會為你提供有關交易和區塊中燃料使用情況的資料，而且有些還會提供有關網路當前燃料價格的資訊。 這將幫助瞭解網路使用情況、提交安全交易並且不會超支燃料。 尋找可以幫助你將此資訊輸入產品介面的應用程式介面。 燃料的特定資料包括：

- 安全但緩慢的交易所需的預估燃料單位（+ 預估價格和持續時間）
- 中等速度交易所需的預估燃料單位（+ 預估價格和持續時間）
- 快速交易所需的預估燃料單位（+ 預估價格和持續時間）
- 基於燃料價格的平均確認時間
- 正在消耗燃料的合約 - 換句話說，正在網路上大量使用的熱門產品
- 正在花費燃料的帳戶 - 換句話說，頻繁使用網路的使用者

### 交易 {#transactions}

區塊瀏覽器已成為追蹤交易進度的常見方式。 這是因為你可以取得的詳細程度提供了額外的確定性。 交易資料包括：

**標準數據**

- 交易雜湊 - 當交易被提交時產生的雜湊
- 狀態 - 指示交易為待處理、失敗還是成功
- 區塊 - 交易被打包進的區塊
- 時間戳 - 交易被納入由驗證者提議的區塊的時間
- 發送者 - 提交此交易的帳戶地址
- 接收者 - 接收者或與交易互動的智慧型合約的地址
- 轉移的代幣 - 做為交易的一部分被轉移的代幣清單
- 價值 - 轉移的以太幣總價值
- 交易費用 - 支付給驗證者處理交易的金額（計算方法為燃料價格\*使用的燃料）

**進階數據**

- 燃料限制 - 此交易最高可消耗多少單位的燃料
- 使用的燃料 - 交易實際消耗的燃料單位量
- 燃料價格 - 每單位燃料的價格
- 隨機數 - `from` 地址的交易編號（注意，隨機數從 0 開始算，所以隨機數 `100` 實際上是此帳戶提交的第 101 筆交易）
- 輸入資料 - 交易所需的任何額外資訊

### 帳戶 {#accounts}

你可以存取有關帳戶的大量資料。 這就是為什麼通常建議使用多個帳戶，以便你的資產和價值不易被追蹤。 還有一些解決方案正在開發中，以使交易和帳戶活動更加私密。 但以下是帳戶可用的資料：

**使用者帳戶：**

- 帳戶地址 - 你可以向其中發送資金的公開地址
- 以太幣餘額 - 該帳戶的以太幣餘額
- 以太幣總價值 - 以太幣的價值
- 代幣 - 與該帳戶有關的代幣及其價值
- 交易記錄 - 此帳戶作為發送者或接受者的所有交易的清單

**智慧型合約**

雖然智慧型合約帳戶擁有使用者帳戶將擁有的所有資料，但某些區塊瀏覽器甚至還會顯示一些程式碼資訊。 範例包含：

- 合約建立者 - 將合約部署至主網的地址
- 建立交易 - 包括將合約部署到主網的交易
- 原始程式碼 - 智慧型合約的 Solidity 或 Vyper 程式碼
- 合約 ABI - 合約的應用程式二進位介面 - 合約進行的呼叫和接收的資料
- 合約建立程式碼 - 智慧型合約經編譯的位元組碼 - 在你編譯以 Solidity 或 Vyper 等語言編寫的智慧型合約時產生
- 合約事件 - 智慧型合約中呼叫的方法的歷史紀錄 - 基本上是查看合約如何使用以及使用頻率的一種方式

### 代幣 {#tokens}

代幣是一種合約，因此它們具有與智慧型合約類似的資料。 但因為它們有價值並且可以交易，因此有額外的資料點：

- 類型 - 是 ERC-20、ERC-721 或其他代幣標準
- 價格 - 如果是 ERC-20，就會有目前市場價值
- 市值 - 如果是 ERC-20，就會有市值（計算方法為價格\*總供應量）
- 總供應量 - 流通的代幣數量
- 持有者 - 持有該代幣的地址數量
- 轉移 - 代幣在帳戶間被轉移的次數
- 交易記錄 - 代幣的所有交易歷史記錄
- 合約地址 - 部署到主網的代幣的地址
- 小數 - ERC-20 代幣是可分割的，且具有小數位

### 網路 {#network}

一些區塊資料更全面地關注以太坊的健康狀況。

- 總交易數量 - 自以太坊建立以來的交易數量
- 每秒交易數量 - 每秒可處理的交易數量
- 以太幣價格 - 目前 1 個以太幣的價值
- 以太幣總供應量 - 流通的以太幣數量 - 請記得，當新區塊建立時，新以太幣會被做為區塊獎勵而產生
- 市值 - 價格\*供應量的計算結果

## 共識層資料 {#consensus-layer-data}

### 時期 {#epoch}

由於安全考量，會在每個時期（每 6.4 分鐘）結束時建立隨機化驗證者委員會。 時期資料包含：

- 時期編號
- 最終狀態 - 時期是否已完成（是/否）
- 時間 - 時期結束的時間
- 證明 - 時期中的證明數量（對時隙內區塊的投票）
- 存款 - 時期內包含的以太幣存款數量（驗證者必須質押以太幣才能成為驗證者）
- 罰沒 - 對區塊提議者或證明者的處罰次數
- 投票參與 - 用於證明區塊的質押以太幣數量
- 驗證者 - 在該時期中活躍的驗證者數量
- 驗證者平均餘額 - 活躍驗證者的平均餘額
- 時隙 - 時期中包含的時隙數量（時隙包含一個有效區塊）

### 時隙 {#slot}

時隙是建立區塊的機會，每個時隙可用的資料包括：

- 時期 - 時隙在其中有效的時期
- 時隙編號
- 狀態 - 時隙狀態（已提議/缺失）
- 時間 - 時隙的時間戳
- 提議者 - 在該時隙提議區塊的驗證者
- 區塊根 - 信標區塊的雜湊樹根
- 父根 - 前一個區塊的雜湊
- 狀態根 - 信標狀態的雜湊樹根
- 簽名
- Randao 揭示
- Graffiti - 區塊提議者可以在其區塊提議中包含 32 位元組的訊息
- 執行資料
  - 區塊雜湊
  - 存款計數
  - 存款根
- 證明 - 此時隙中的區塊的證明數量
- 存款 - 此時隙內的存款數量
- 自願退出 - 此時隙內退出的驗證者數量
- 罰沒 - 對區塊提議者或證明者的處罰次數
- 投票 - 此時隙中為區塊投票的驗證者

### 區塊 {#blocks-1}

權益證明將時間分割為時期與時隙。 這意味著新資料！

- 提議者 - 經演算法選出的提議新區塊的驗證者
- 時期 - 提議區塊的時期
- 時隙 - 提議區塊的時隙
- 證明 - 時隙中包含的證明數量 - 證明就像投票一樣，表示區塊已準備好進入信標鏈

### 驗證者 {#validators}

驗證者負責在時隙內提議區塊並證明區塊。

- 驗證者編號 - 代表驗證者的唯一編號
- 目前餘額 - 驗證者的餘額（包含獎勵）
- 有效餘額 - 驗證者用於質押的餘額
- 收入 - 驗證者收到的獎勵或處罰
- 狀態 - 驗證者目前是否在線和是否活躍
- 證明有效性 - 驗證者的證明被加入鏈上的平均時間
- 啟用資格 - 驗證者可以開始驗證的日期（和時期）
- 啟用開始時間 - 驗證者的啟用日期（和時期）
- 提議的區塊 - 驗證者提議的區塊
- 證明 - 驗證者提供的證明
- 存款 - 發送者地址、交易雜湊、區塊編號、時間戳、驗證者的質押存款金額及狀態

### 證明 {#attestations}

證明是投票「同意」將區塊包含在鏈中。 它們的資料與證明紀錄和進行證明的驗證者相關。

- 時隙 - 證明發生的時隙
- 委員會索引 - 在給定時隙的委員會的索引
- 聚合位元 - 表示證明中所有參與驗證者的聚合證明
- 驗證者 - 提供證明的驗證者
- 信標區塊根 - 指向驗證者正在證明的區塊
- 來源 - 指向最新的已證明時期
- 目標 - 指向最新的時期邊界
- 簽名

### 網路 {#network-1}

共識層頂層資料包括以下內容：

- 目前時期
- 目前時隙
- 活躍驗證者 - 活躍驗證者的數量
- 等待中驗證者 - 等待啟用的驗證者數量
- 質押的以太幣 - 網路中質押的以太幣數量
- 平均餘額 - 驗證者的平均以太幣餘額

## 區塊瀏覽器 {#block-explorers}

- [Etherscan](https://etherscan.io/) - 可用於擷取以太坊主網及 Goerli 測試網資料的區塊瀏覽器
- [3xpl](https://3xpl.com/ethereum) - 一個允許下載其資料集的無廣告開源以太坊瀏覽器
- [Beaconcha.in](https://beaconcha.in/) -用於以太坊主網及 Goerli 測試網的開源區塊瀏覽器
- <0>Blockchair</0> -- 最私密的以太坊瀏覽器。 也用於排序和篩選（記憶體池）資料
- [Etherchain](https://www.etherchain.org/) - 以太坊主網的區塊瀏覽器
- [Ethplorer](https://ethplorer.io/) - 專為以太坊主網及 Kovan 測試網代幣打造的區塊瀏覽器
- [Rantom](https://rantom.app/) - 方便使用的開源去中心化金融及非同質化代幣交易檢視器，可提供詳細的訊息
- [Ethernow](https://www.ethernow.xyz/) - 即時交易瀏覽器，讓你能夠查看以太坊主網鏈前層

## 延伸閱讀 {#further-reading}

_知道一個曾經幫助你學習更多社區或社團資源? 歡迎在本頁自由編輯或添加內容！！_

## 相關主題 {#related-topics}

- [交易](/developers/docs/transactions/)
- [帳戶](/developers/docs/accounts/)
- [網路](/developers/docs/networks/)