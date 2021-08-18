---
description: 服務控制管理員 (SCM) 會將服務控制事件傳送至服務控制處理常式常式，藉以控制服務。
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: 多執行緒服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32b4b51f740e0a3773115b9048ec34619910936f1531fba1260740df28873b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003726"
---
# <a name="multithreaded-services"></a>多執行緒服務

服務控制管理員 (SCM) 會將服務控制事件傳送至服務的控制處理常式常式，藉以控制服務。 服務必須及時地回應控制事件，讓 SCM 可以追蹤服務的狀態。 此外，服務的狀態必須符合 SCM 所接收之狀態的描述。

由於服務與 SCM 之間的通訊機制，在服務中使用多個執行緒時，您必須特別小心。 當服務指示由 SCM 停止時，它必須等待所有線程結束，然後再向 SCM 報表服務已停止。 否則，SCM 可能會混淆服務的狀態，而且可能無法正確關閉。

SCM 必須收到通知，表示服務正在回應停止控制事件，且正在停止服務。 如果 [**)  (**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) 服務在 **>setservicestatus** 的前一次呼叫中所指定的時間內 (wait 提示) 所指定的時間內，且檢查點更新為大於先前呼叫 **>setservicestatus** 所指定的檢查點，則 SCM 會假設服務正在進行中。

如果服務向 SCM 回報在所有線程都結束之前已停止，則 SCM 可能會將其解釋為衝突。 這可能會導致無法停止或重新開機服務的狀態。

 

 



