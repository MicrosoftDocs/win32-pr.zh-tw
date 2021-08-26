---
title: 暫停狀態
description: 在連接操作期間，遠端伺服器可能會在沒有本機使用者的其他資訊的情況下繼續進行。
ms.assetid: a1a36b2a-33df-4cba-85a6-f4225779cd63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec66a63adbee524ec231b5c9dd9b0b410c8f4fbc73746ae9b924294c680b4a9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029138"
---
# <a name="paused-states"></a>暫停狀態

在連接操作期間，遠端伺服器可能會在沒有本機使用者的其他資訊的情況下繼續進行。 從 Windows NT 3.5 開始， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)函數支援暫停狀態。 暫停狀態可讓遠端存取連線管理員暫停線上作業，讓 RAS 用戶端應用程式可以從使用者收集資訊。

暫停狀態在下列情況下很有用：

-   當使用者需要提供 [回呼](callback-connections.md) 號碼時。
-   當使用者驗證失敗時，使用者可以輸入不同的使用者名稱和密碼。
-   當使用者的密碼過期時，使用者可以提供新的密碼。

預設會停用暫停狀態支援。 想要支援暫停狀態的 RAS 用戶端，必須 \_ 在以參數形式傳遞至 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)的 [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85))結構中，設定 RDEOPTS PausedStates 旗標。

當暫停狀態發生時，遠端存取連線管理員會叫用用戶端的通知處理常式。 如果停用暫停狀態支援，則通知訊息會指出錯誤，且連接作業會失敗。 若已啟用，連線管理員會暫停連線作業以等候 RAS 用戶端的回應。 RAS 用戶端可以透過第二個 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫來繼續連線作業，或呼叫 [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) 函式將它終止。

取得使用者的輸入之後，RAS 用戶端會重新開機連接作業，方法是再次呼叫 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 。 第二個 **RasDial** 呼叫必須指定下列資訊：

-   原始 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫所傳回的連接控制碼。
-   與原始 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫相同的通知處理常式。
-   使用者在 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) 結構中適當的成員輸入。 **RASDIALPARAMS** 結構的其他成員應具有與原始 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫中所指定的相同資訊。

無法從通知處理常式內進行第二個 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 呼叫。

 

 