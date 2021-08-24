---
title: 動態資料交換
description: 本節提供針對無法使用動態資料交換管理程式庫 (DDEML) 的應用程式，執行動態資料交換的指導方針。
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- 動態資料交換 (的 DDE) ，關於
- DDE (動態資料交換) ，關於
- '資料交換、動態資料交換 (DDE) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db58f1027f0dfaacf28c4b2ec8d4208747929b0d40ca55d7d377831777f78a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678038"
---
# <a name="dynamic-data-exchange"></a>動態資料交換

本節提供針對無法使用動態資料交換管理程式庫 (DDEML) 的應用程式，執行動態資料交換的指導方針。 如需 DDEML 的詳細資訊，請參閱[動態資料交換管理程式庫](dynamic-data-exchange-management-library.md)。

### <a name="overviews"></a>概觀



| 名稱                                                           | 描述                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [關於動態資料交換](about-dynamic-data-exchange.md) | 討論如何在應用程式之間傳輸資料。<br/>       |
| [使用動態資料交換](using-dynamic-data-exchange.md) | 提供有關動態資料交換的程式碼範例。<br/> |
| [DDE 參考](dynamic-data-exchange-reference.md)           | API 參考。<br/>                                      |



 

### <a name="dde-functions"></a>DDE 函數



| 名稱                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | 指定服務品質 (QOS) 原始動態資料交換 (dde) 應用程式想要在未來所起始的 dde 交談。 指定的 QOS 適用于這些設定都已開始的任何交談。 DDE 交談的服務品質會在交談期間持續進行;交談期間對 [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) 函式的呼叫不會影響交談的 QOS。 <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | 釋出已張貼之 DDE 訊息的 *lParam* 參數所指定的記憶體。 接收已張貼之 DDE 訊息的應用程式應該在使用 [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) 函式將 *lParam* 值解壓縮之後，呼叫此函式。 <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | 讓 DDE 伺服器應用程式模擬 DDE 用戶端應用程式的安全性內容。 這可防止未經授權的 DDE 用戶端進行安全的伺服器資料。 <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | 將 DDE *lParam* 值封裝成用來在進程之間共用 dde 資料的內部結構。<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | 讓應用程式重複使用已壓縮的 DDE *lParam* 參數，而不是配置新的封裝 *lParam*。 使用此函式可減少傳遞已封裝之 DDE 訊息之應用程式的重新分配。 <br/>                                                                                                                                                                                                                                                          |
| [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | 解壓縮從張貼的 DDE 訊息接收的 DDE *lParam* 值。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>DDE 訊息



| 名稱                                         | 描述                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ 起始**](wm-dde-initiate.md) | 起始與伺服器應用程式的交談，回應指定的應用程式和主題名稱。 收到此訊息時，所有名稱符合指定之應用程式且支援指定主題的伺服器應用程式，都應該要知道它。<br/> |



 

### <a name="dde-notifications"></a>DDE 通知



| 名稱                                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ ACK**](wm-dde-ack.md)             | Nnotifies 接收和處理下列訊息的 DDE 應用程式： [**WM \_ dde \_**](wm-dde-poke.md)傳送、 [**wm \_ dde \_ 執行**](wm-dde-execute.md)、 [**wm \_ dde \_ 資料**](wm-dde-data.md)、 [**Wm \_ dde \_**](wm-dde-advise.md)、wm、 [**wm \_ dde \_ UNADVISE**](wm-dde-unadvise.md)、 [**wm \_ dde \_ 初始**](wm-dde-initiate.md)或 [**wm \_ dde \_ 要求**](wm-dde-request.md) (在某些情況下) 。 <br/> |
| [**WM \_ DDE \_ 建議**](wm-dde-advise.md)       | DDE 用戶端應用程式會將 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息張貼至 DDE 伺服器應用程式，要求伺服器在專案變更時，提供資料項目的更新。 <br/>                                                                                                                                                                                                              |
| [**WM \_ DDE \_ 資料**](wm-dde-data.md)           | DDE 伺服器應用程式會將 [**WM \_ DDE 的 \_ 資料**](wm-dde-data.md) 訊息張貼至 DDE 用戶端應用程式，以將資料項目傳遞給用戶端，或通知用戶端資料項目目的可用性。 <br/>                                                                                                                                                                                                           |
| [**WM \_ DDE \_ 執行**](wm-dde-execute.md)     | DDE 用戶端應用程式會將 [**WM \_ DDE \_ 執行**](wm-dde-execute.md) 訊息張貼至 dde 伺服器應用程式，以將字串傳送至伺服器，以做為一系列的命令來處理。 伺服器應用程式預期會在回應中公佈一則 [**WM 的 \_ DDE \_ ACK**](wm-dde-ack.md) 訊息。 <br/>                                                                                                                      |
| [**WM \_ DDE 的進行 \_**](wm-dde-poke.md)           | DDE 用戶端應用程式會將一封 [**WM \_ dde \_**](wm-dde-poke.md) 郵件訊息張貼至 DDE 伺服器應用程式。 用戶端會使用此訊息要求伺服器接受未請求的資料項目。 伺服器預期會以 [**WM \_ DDE \_**](wm-dde-ack.md) 通知訊息來回複，指出它是否接受該資料項目。 <br/>                                                                                   |
| [**WM \_ DDE \_ 要求**](wm-dde-request.md)     | DDE 用戶端應用程式會將 [**WM \_ DDE \_ 要求**](wm-dde-request.md) 訊息張貼至 DDE 伺服器應用程式，以要求資料項目的值。 <br/>                                                                                                                                                                                                                                                              |
| [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) | DDE 應用程式 (用戶端或伺服器) 張貼 [**WM \_ DDE \_ 終止**](wm-dde-terminate.md) 訊息以終止交談。 <br/>                                                                                                                                                                                                                                                                                  |
| [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)   | DDE 用戶端應用程式會張貼一個 [**WM \_ dde \_ UNADVISE**](wm-dde-unadvise.md) 訊息，通知 dde 伺服器應用程式，該專案的指定專案或特定剪貼簿格式不應再更新。 這會終止指定專案的暖或經常性存取資料連結。 <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>DDE 結構



| 名稱                           | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | 包含將 DDE 應用程式傳遞給其夥伴作為 [**WM \_ DDE \_ ACK**](wm-dde-ack.md) 訊息一部分的狀態旗標。 旗標會提供應用程式的相關詳細資料，內容為 [**wm： wm \_ dde \_ 資料**](wm-dde-data.md)、 [**wm \_ dde \_**](wm-dde-poke.md)郵件、 [**wm \_ dde \_ 執行**](wm-dde-execute.md)、 [**wm \_ dde \_ 建議**](wm-dde-advise.md)、 [**wm \_ dde \_ UNADVISE**](wm-dde-unadvise.md)和 [**wm \_ dde \_ 要求**](wm-dde-request.md)的訊息。 <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | 包含旗標，這些旗標會指定 DDE 伺服器應用程式在建議迴圈期間如何傳送資料給用戶端應用程式。 用戶端會將 [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) 結構的控制碼傳遞給伺服器，作為 [**WM \_ DDE \_ 建議**](wm-dde-advise.md) 訊息的一部分。 <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | 包含傳送為 [**WM \_ DDE \_ 資料**](wm-dde-data.md) 訊息一部分的資料和資料相關資訊。 <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | 包含資料和資料的相關資訊，這些資訊會隨著 [**WM \_ DDE \_**](wm-dde-poke.md) 訊息傳送。 <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | 包含 DDE 服務名稱和主題名稱。 在 [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) 交易期間，DDE 伺服器應用程式可以使用此結構來列舉所支援的服務-主題配對。 <br/>                                                                                                                                                                                                                                                   |



 

 

 





