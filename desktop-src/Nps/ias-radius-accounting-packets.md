---
title: 使用網路原則伺服器進行記錄
description: 使用網路原則伺服器進行記錄
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315838"
---
# <a name="logging-with-network-policy-server"></a>使用網路原則伺服器進行記錄

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

下表僅說明 RADIUS 帳戶處理封包的最重要層面。 註釋檔的 RADIUS 帳戶處理要求 ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) 提供這些封包的詳細資訊。

RADIUS 帳戶處理封包可以分為下列類別。



| 帳戶處理封包  | Description                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | 由網路存取伺服器傳送 (NAS) ，以指出它已重新開機。<br/> 包含 nas 識別碼/ipaddress。<br/>                                                                                        |
| Accounting-Off     | 由 NAS 傳送以表示正在關閉。<br/> 包含 nas 識別碼/ipaddress。<br/>                                                                                                            |
| Accounting-Start   | 由 NAS 在使用者經過驗證和授權之後傳送，以指出使用者會話的啟動。 <br/> 包含 userid、nas 識別碼/ipaddress，以及從 NAS 接收的其他資訊。<br/> |
| Accounting-Stop    | 由 NAS 傳送以表示使用者會話的結束。<br/> 包含 userid、nas 識別碼/ipaddress，以及從 NAS 接收的其他資訊。<br/>                                                      |
| Accounting-Interim | 可能會由 NAS 定期傳送到 NAS 上登入的每位使用者。 <br/> 這項功能在較新版本的 NAS 中通常會受到支援。<br/>                                                     |



 

收集可透過 RADIUS 取得的帳戶處理資訊時，請務必考慮下列問題：

-   在罕見的情況下，封包可能會在傳輸期間遺失，且可能永遠不會到達 RADIUS 伺服器。
-   如果 NAS 中止，RADIUS 伺服器就不會收到通知。
-   ISDN 支援多個會話，且每個會話都會產生一組計量啟動/停止封包。 有一個會計屬性稱為多會話識別碼，可清楚識別這類多會話封包。 除了會話識別碼之外，請檢查多會話識別碼，以計算會話的數目。

## <a name="requests-logged-by-nps"></a>NPS 所記錄的要求

NPS 預設不會記錄任何資料。 NPS 可以使用 nps 使用者介面 (node.js) 來進行設定，以記錄下列要求。



| 記錄的封包          | Description                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 帳戶處理要求     | 上表中所述的任何會計封包。<br/>                                                                    |
| 驗證要求 | 由 NAS 代表連接的使用者傳送。<br/> 記錄專案只包含傳入屬性。<br/>                    |
| 驗證接受  | 由 NPS 傳送以表示應接受使用者連接。<br/> 記錄專案只包含傳出屬性。<br/> |
| 驗證拒絕  | 由 NPS 傳送，以指出應該拒絕使用者連接。<br/> 記錄專案只包含傳出屬性。<br/> |



 

NPS 所記錄的資料可以移至 NPS 伺服器上的文字檔，或移至中央 SQL 資料庫。 如需 NPS SQL 記錄的詳細資訊，請參閱 [sql](sql-programmability.md)程式設計。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網際網路驗證服務和網路原則伺服器](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS 驗證、授權和帳戶處理](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[使用狀態伺服器](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

