---
title: 服務的指導方針
description: 服務應遵守這些指導方針，以確保重新開機管理員可以在必要時關閉和重新開機服務，以安裝更新。 應用程式可以使用應用程式指導方針中所述的指導方針。
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51374c0a4c6fc561b8259aadf15e3d5487e12483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023817"
---
# <a name="guidelines-for-services"></a>服務的指導方針

服務應遵守這些指導方針，以確保重新開機管理員可以在必要時關閉和重新開機服務，以安裝更新。 應用程式可以使用 [應用程式指導方針](guidelines-for-applications.md)中所述的指導方針。

-   服務應該能夠使用 [服務控制管理員](/windows/desktop/Services/service-control-manager) 來關閉和重新開機，而不需要重新開機系統。 此指導方針的例外狀況是在 lsass.exe 或 services.exe 內容中執行的重要系統進程。
-   重新開機管理員會接受服務相關性。 當服務關閉並重新啟動時，其相依服務會關閉並重新啟動。
-   服務應該會在 [服務控制管理員 (SCM) ](/windows/desktop/Services/service-control-manager)中指定復原間隔和重設期間。 復原間隔是 SCM 在取得復原動作之前等候的最後一次失敗之後的時間（以毫秒為間隔）。 重設期間是在最後一次失敗之後，服務控制管理員在將失敗計數重設為0之前等候的時間（以秒為單位）。 服務可以使用 [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) 函數來變更設定。

    [重要服務](critical-system-services.md) 應該使用下列復原設定，指定在第一次失敗之後重新開機服務、在第二次失敗後重新開機兩分鐘，以及在第三次失敗之後重新開機電腦一分鐘。 失敗計數會在300秒後重設為0。

    <dl> 復原動作：重新開機/60000/重新開機/120000/重新開機/60000 & 重設 = 300  
    </dl>

    [重要服務](critical-system-services.md) 應該在非關鍵服務之前啟動。 非關鍵服務的服務應該使用下列復原設定，指定在第一次失敗之後，重新開機服務兩分鐘。 這項服務不會在第二次失敗之後重新開機，而且系統管理員必須在這種情況下介入。 失敗計數會在900秒後重設為0。

    <dl> 復原動作： Restart/120000/Restart/300000/None/0 & Reset = 900  
    </dl>

 

 