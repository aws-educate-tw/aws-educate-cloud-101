# 2. Amazon Elastic Computing Cloud (Amazon EC2)

# 🖥️ Amazon ****EC2****

---

Amazon Elastic Compute Cloud (Amazon EC2) 是一種 Web 服務，在雲端提供可調整大小的運算容量。使用者操作 Amazon EC2 時可依據自身需求啟動任意數量的虛擬伺服器 (執行個體)，並設定安全性、聯網功能以及管理儲存。由於Amazon EC2 具備快速擴展與縮減規模的特性，非常適合處理服務流量高峰的需求，解決使用者預測流量的問題。Amazon EC2 也減少開發前期所需的硬體投資，讓使用者可以更快速開發並部署應用程式。

# 💽 ****Amazon Machine Image (AMI)****

---

Amazon Machine Image (AMI) 提供啟動執行個體所需的資訊，而執行個體是雲端中的虛擬伺服器。在啟動執行個體時，必須指定 AMI，AMI 包括下列項目：

- 執行個體根磁碟區的範本 (例如：作業系統、應用程式和安裝了應用程式的伺服器)
- 啟動許可：控制哪些 AWS 帳戶可以使用該 AMI 來啟動執行個體
- 區塊型設備映射：指定執行個體啟動時要與其連接的磁碟區

**Quick Start** (快速啟動) 清單包含最常用的 AMI。使用者也可以建立自己的 AMI，或者從 AWS Marketplace 選取 AMI。AWS Marketplace 是一個線上商店，使用者可以在此銷售或購買在 AWS 上執行的軟體。

# 🔑 ****金鑰對 Key pair****

---

Amazon EC2 會使用公有金鑰密碼，將登入資訊加密及解密。若要登入執行個體，必須建立金鑰對，在啟動執行個體時指定金鑰對的名稱，並在連線至執行個體時提供私有金鑰。