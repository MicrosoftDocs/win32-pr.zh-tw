---
title: IAgentCharacter HasOtherClients
description: IAgentCharacter HasOtherClients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507468"
---
# <a name="iagentcharacterhasotherclients"></a>IAgentCharacter::HasOtherClients

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

抓取字元是否有其他用戶端。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*
</dt> <dd>

變數的位址，此變數會接收其他已連線用戶端數目 (用戶端數目減去用戶端) 的用戶端總數。

</dd> </dl>

 

 




