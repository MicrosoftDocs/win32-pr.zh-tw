---
title: 使用遠端桌面虛擬化 API
description: 開發人員可以使用此 API 來自訂 RD 連線代理人用來判斷連入用戶端連線最佳目的地的邏輯。
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- 使用虛擬化 API 遠端桌面服務遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9ebfc014a2c8ec20d299bbb8be9183b25ce89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375552"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>使用遠端桌面虛擬化 API

終端機服務會話目錄 (TS 會話目錄) 角色服務可讓終端機伺服器將使用者和會話資訊儲存在稱為會話目錄的資料庫中。 當使用者連線到伺服器陣列中的終端機伺服器時，TS 會話目錄會判斷使用者是否已在終端機伺服器上執行會話，如果是，則會將使用者重新導向至該終端機伺服器。

在 Windows Server 2008 中，TS 會話目錄角色服務已展開並重新命名為「終端機服務會話代理人」 (TS 會話代理程式) 。 除了維護現有會話的目錄之外，TS 會話代理人也可以 Broker 連入連線。 當 TS 會話代理人接收來自使用者的連入連線時，它會檢查其資料庫，以判斷使用者是否在終端機伺服器上有現有的會話。 如果是，TS 會話代理人會將連線重新導向至相同的終端機伺服器。 如果沒有，則 TS 會話代理人會判斷哪一個終端機伺服器的連線最少，並將連接重新導向至該伺服器。

從 Windows Server 2008 開始，Microsoft 也發行了公用應用程式開發介面， (API) 來監視和與終端機伺服器上的會話互動。 [遠端桌面連線代理人外掛程式參考](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)中會說明此 API。 開發人員可以使用此 API 來建立自訂原則外掛程式，以覆寫 TS 會話代理人的標準重新導向邏輯。 自訂外掛程式可將會話重新導向到終端機伺服器，以及虛擬機器、虛擬桌面、blade 伺服器和實體桌面。

在 Windows Server 2008 R2 中，遠端桌面連線代理人 (RD 連線代理人)  (先前稱為「TS 會話代理人) 」的架構已擴充為支援虛擬機器的連線。 新的架構可透過遠端桌面虛擬化 API 支援虛擬機器的會話管理。 開發人員可以使用此 API 來自訂 RD 連線代理人用來判斷連入用戶端連線最佳目的地的邏輯。

遠端桌面虛擬化 API 為開發人員提供了多項優點：

-   使用實體終端機伺服器的介面類別似于使用虛擬機器的介面。
-   開發人員可以取代所有或部分的標準重新導向邏輯。 開發人員可以建立產品隨附的程式碼，而不需要從頭開始撰寫所有專案。
-   管理伺服器或會話中不需要其他管理代理程式。
-   仍支援為了與 Windows Server 2008 一起使用而開發的 TS 會話代理人外掛程式。
-   此 API 也可讓開發人員建立使用者介面，以管理遠端桌面工作階段主機 (RD 工作階段主機) 伺服器 (先前稱為「終端機伺服器」 ) 和虛擬機器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[遠端桌面虛擬化 API 參考](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[遠端桌面連線代理人外掛程式參考](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 