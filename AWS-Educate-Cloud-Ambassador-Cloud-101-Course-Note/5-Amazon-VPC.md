# 5. Amazon Virtual Private Cloud (Amazon VPC)

![*image src: awseducate.com*](5%20Amazon%20Virtual%20Private%20Cloud%20(Amazon%20VPC)%20622a4d700a59468d812f375e6e077bc6/%25E8%259E%25A2%25E5%25B9%2595%25E6%2593%25B7%25E5%258F%2596%25E7%2595%25AB%25E9%259D%25A2_2022-09-21_150544.png)

*image src: awseducate.com*

# ☁️ 虛擬私有雲VPC

---

VPC 是一種專供 Amazon Web Services (AWS) 帳戶使用的虛擬網路。在邏輯上，它與 AWS 雲端中的其他虛擬網路隔離。您可以將 AWS 資源啟動至 VPC，例如 Amazon Elastic Compute Cloud (Amazon EC2) 執行個體。您可以修改 VPC 的 IP 地址範圍並且可以建立子網路來設定 VPC。您也可以設定路由表、網路閘道和安全設定。

# 🚧 子網路

---

![*image src: awseducate.com*](5%20Amazon%20Virtual%20Private%20Cloud%20(Amazon%20VPC)%20622a4d700a59468d812f375e6e077bc6/%25E8%259E%25A2%25E5%25B9%2595%25E6%2593%25B7%25E5%258F%2596%25E7%2595%25AB%25E9%259D%25A2_2022-09-21_151620.png)

*image src: awseducate.com*

子網路是您的 VPC 中的 IP 地址範圍。子網必須位於單一可用區域。新增子網之後，您可以在 VPC 中部署 AWS 資源。

---

- 公有子網路(Public Subnet): 子網流量透過網際網路閘道或僅傳出網際網路閘道路由至公有網際網路。
- 私有子網路(Private Subnet): 子網流量無法透過網際網路閘道或僅傳出網際網路閘道連線至公有網際網路。

# 🌐 網際網路閘道

---

閘道會將 VPC 連線至另一個網路。例如，您可使用網際網路閘道將 VPC 連線至網際網路。

---

- 在路由表中提供連接到網際網路的目標
- 針對被指派公有 IPv4 地址的執行個體執行網路位置轉譯 (NAT)

# 🔃 路由表

---

使用路由表決定子網或閘道中的網路流量導向何處。

# 🔒 應用程式安全群組

---

安全群組會做為執行個體的虛擬防火牆，以控制傳入和傳出流量。安全群組在執行個體的彈性網路界面層級運作。安全群組不在子網路層級運作。因此，每個執行個體都可以有自己的防火牆來控制流量。如果您在啟動時未指定特定的安全群組，系統會自動將執行個體指派給 VPC 的預設安全群組。