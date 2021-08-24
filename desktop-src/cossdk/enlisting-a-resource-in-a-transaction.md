---
description: 在交易中登記資源
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: 在交易中登記資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef1ab34d32853be0ca7d4641958b4f57ab55577865aad8612821e98882c71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858958"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>在交易中登記資源

配置資源之後，但在將資源傳回給資源配置器之前，分配器管理員會檢查 COM + 以查看呼叫物件是否正在交易內執行。 如果呼叫的物件是在交易內執行，則分配器管理員會回呼至資源配置器，並要求它在交易中登記資源。 然後，資源會傳回給資源配置器，然後將它傳回給呼叫的實例。

資源配置器必須能夠在具有分散式交易協調器 (DTC) 的 OLE 交易中登記。

> [!Note]  
> 當資源配置不表達非交易資源（例如記憶體或執行緒）時，交易登記是選擇性的。

 

當交易完成時，COM + 會通知分配者管理員其是否已認可或中止。 然後，分配者管理員會通知每個資源配置器的持有者，此交易中登記的任何資源現在都可以移至一般清查。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 資源配置器概念](com--resource-dispenser-concepts.md)
</dt> <dt>

[適用于 COM + 資源配置器的共用資源狀態](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[資源配置器資源配置進程](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



