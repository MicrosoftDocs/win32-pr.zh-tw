---
description: 服務程式包含一或多個服務的可執行程式碼。
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: 服務程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebc2f696d321983487442be232e5d5a2278090a9c374e98b412522914e6c1ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967331"
---
# <a name="service-programs"></a>服務程式

*服務程式* 包含一或多個服務的可執行程式碼。 以類型服務 WIN32 本身的進程建立的服務程式 \_ \_ \_ 只包含一項服務的程式碼。 以類型服務 \_ WIN32 共用進程建立的服務 \_ 程式 \_ 包含多項服務的程式碼，讓它們可以共用程式碼。 執行這項服務程式的其中一個範例，就是裝載內部 Windows 服務的一般服務主機進程 Svchost.exe。 請注意，Svchost.exe 是保留給作業系統使用，不應由非 Windows 的服務使用。 相反地，開發人員應該執行自己的服務裝載程式。

服務程式可以設定為從內建 (本機) 、主要或受信任網域的使用者帳戶內容中執行。 您也可以將它設定為在特殊的 [服務使用者帳戶](service-user-accounts.md)中執行。

下列主題描述服務程式必須包含的 [服務控制管理員](service-control-manager.md) (SCM) 的介面需求：

-   [服務進入點](service-entry-point.md)
-   [服務 ServiceMain 函式](service-servicemain-function.md)
-   [服務控制處理函式](service-control-handler-function.md)

這些主題並不適用于驅動程式服務。 如需驅動程式服務的介面需求，請參閱 Windows 驅動程式套件 (WDK) 。

服務會以背景進程的形式執行，可能會影響系統效能、回應能力、能源效率和安全性。 如需服務優化指導方針，請參閱針對[Windows 開發有效率的背景流程](/windows-hardware/drivers/kernel/implementing-power-management)。 下列主題將描述其他程式設計考慮：

-   [服務狀態轉換](service-status-transitions.md)
-   [接收服務中的事件](receiving-events-in-a-service.md)
-   [多執行緒服務](multithreaded-services.md)
-   [服務和登錄](services-and-the-registry.md)
-   [服務和重新導向的磁片磁碟機](services-and-redirected-drives.md)
-   [服務觸發程式事件](service-trigger-events.md)

請注意，如果服務程式是以 RPC 伺服器的方式運作，則應該使用動態端點和相互驗證。

 

 
