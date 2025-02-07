# V5: 網路通訊規範

## 管理目標

本節中列出的管理目標是確保行動應用程式和遠端服務之間交換的訊息的機密性和完整性。確保行動應用程式必須使用 TLS 協議為網路傳輸作為安全加密的通道。L2 列出了其他加強防禦措施，例如 SSL 固定。

## 安全驗證要求

| # | MSTG-ID | 描述 | L1 | L2 |
| --- | --- | --- | --- | --- |
| **5.1** | MSTG‑NETWORK‑1 | APP 網路傳輸資料均使用 TLS 協議作為加密協定. | ✓ | ✓ |
| **5.2** | MSTG‑NETWORK‑2 | TLS 協定使用，必須符合目前業界規範，如已通報不安全的協定標準，須立即修正。 | ✓ | ✓ |
| **5.3** | MSTG‑NETWORK‑3 | 在與遠端建立資料傳輸通道時，須先驗證 X.509 證書，且只能接受有簽名受信任的 CA 憑證。 | ✓ | ✓ |
| **5.4** | MSTG‑NETWORK‑4 | 應用程式中公鑰和數位憑證來確保系統資訊安全，並不能隨意與不明遠端建立連線，提供受信任 CA 憑證. |   | ✓ |
| **5.5** | MSTG‑NETWORK‑5 | 應用程式的相關重要操作，不可只依賴單一方式驗證（如電子郵件或者 SMS) |  | ✓ |
| **5.6** | MSTG‑NETWORK‑6 | 應用程式需隨時更新連接方式以及資料庫安全性 |  | ✓ |

## 參考

OWASP Mobile Security Testing Guide 提供了有關驗證本章節中列出的準則的詳細使用說明。

- Android - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x05g-Testing-Network-Communication.md>
- iOS - <https://github.com/OWASP/owasp-mstg/blob/master/Document/0x06g-Testing-Network-Communication.md>

更多相關信息，另請參閱：

- OWASP Mobile Top 10: M3 (Insecure Communication) - <https://www.owasp.org/index.php/Mobile_Top_10_2016-M3-Insecure_Communication>
- CWE 319 (Cleartext Transmission of Sensitive Information) - <https://cwe.mitre.org/data/definitions/319.html>
- CWE 295 (Improper Certificate Validation) - <https://cwe.mitre.org/data/definitions/295.html>
