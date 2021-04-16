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
# <a name="iagentcharacterhasotherclients"></a><span data-ttu-id="c0023-103">IAgentCharacter::HasOtherClients</span><span class="sxs-lookup"><span data-stu-id="c0023-103">IAgentCharacter::HasOtherClients</span></span>

<span data-ttu-id="c0023-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="c0023-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

<span data-ttu-id="c0023-105">抓取字元是否有其他用戶端。</span><span class="sxs-lookup"><span data-stu-id="c0023-105">Retrieves whether a character has other clients.</span></span>

-   <span data-ttu-id="c0023-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="c0023-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c0023-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span><span class="sxs-lookup"><span data-stu-id="c0023-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span></span>
</dt> <dd>

<span data-ttu-id="c0023-108">變數的位址，此變數會接收其他已連線用戶端數目 (用戶端數目減去用戶端) 的用戶端總數。</span><span class="sxs-lookup"><span data-stu-id="c0023-108">Address of a variable that receives the number of other connected clients for the character (total number of clients minus your client).</span></span>

</dd> </dl>

 

 




