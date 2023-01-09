# 6. AWS Identity and Access Management (IAM)

# 🔏 AWS Identity and Access Management (IAM)

---

AWS Identity and Access Management (IAM) 是一種 Web 服務，讓您能夠安全地控制對 AWS 資源的存取。您可以使用 IAM 來控制能通過身分驗證 (登入) 和授權使用資源的 (具有許可) 的人員。

# 👤 使用者 User

---

IAM 使用者是您在 AWS 中建立的實體。IAM 使用者表示使用 IAM 使用者與 AWS 互動的人員或服務。IAM 使用者主要用於讓人們能夠登入 AWS Management Console 進行互動式任務，並使用 API 或 CLI 以編寫程式的方式對 AWS 服務發出請求。AWS 中的使用者由名稱、用於登入 AWS Management Console的密碼，以及最多兩個可與 API 或 CLI 一起使用的存取金鑰組成。當您建立 IAM 使用者時，透過使其成為連接到適當許可政策的使用者群組成員 (建議)，或透過直接將政策連接到使用者來授予其許可。您也可以複製現有 IAM 使用者的許可，這會自動使新使用者成為相同使用者群組的成員並連接所有相同的政策。

# 👥 群組 Group

---

IAM 使用者群組是 IAM 使用者的集合。您可以使用使用者群組來指定使用者集合的許可，這可以使這些使用者更輕鬆地管理這些許可。例如，您可以擁有一個名為 *Admins*的使用者群組，並為該使用者群組提供管理員通常需要的許可類型。該使用者群組中的任何使用者都自動擁有指派至該使用者群組的許可。如果新使用者加入您的組織並擁有管理員許可，您可以透過將使用者新增到該使用者群組來分配適當的許可。

# 💼 IAM 商業案例

---

- 貴公司使用越來越多的 AWS 服務，這包含許多 Amazon EC2 執行個體和大量的 Amazon S3 儲存貯體。您想要根據工作職能給予新進員工存取權，如下表所示：

| 使用者 | 所屬群組 | 許可 |
| --- | --- | --- |
| user-1 | S3-Support | 對 Amazon S3 的唯讀存取權 |
| user-2 | EC2-Support | 對 Amazon EC2 的唯讀存取權 |
| user-3 | EC2-Admin | 檢視、啟動和停止 Amazon EC2 執行個體 |