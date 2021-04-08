---
title: 事件凍結
description: 事件凍結
ms.assetid: 1e537503-f7e7-42f4-aa3c-3c71715b84fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e403448d53949c263b8e146961690de1200436c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839928"
---
# <a name="event-freezing"></a>事件凍結

容器可透過呼叫 [**IOleControl：： FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) 和 **TRUE**，通知控制項尚未準備好回應事件。 它可以藉由呼叫 **FreezeEvents** 和 **FALSE** 來解除凍結事件。 當容器凍結事件時，它會凍結事件處理，而不是事件接收;也就是說，當事件凍結時，容器仍然可以接收事件。 如果容器在事件被凍結時收到事件通知，容器應忽略該事件。 沒有其他適用的動作。

如果控制項對 [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)的呼叫很重要，則控制項應該要記下容器的呼叫，如果沒有遺漏 **事件的話。** 當容器的事件處理被凍結時，控制項應該執行下列其中一項技術：

-   引發事件，瞭解容器不會採取任何動作的完整知識。
-   捨棄控制項將引發的所有事件。
-   將所有暫止的事件排入佇列，並在容器以 **FALSE** 呼叫 [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)之後引發這些事件。
-   只將相關或重要的事件排入佇列，並在容器以 **FALSE** 呼叫 [**FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)之後引發這些事件。

在不同的情況下，每個技巧都是可接受的。 控制項開發人員負責決定和執行控制項功能的適當技術。

 

 




