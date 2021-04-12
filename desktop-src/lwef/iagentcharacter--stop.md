---
title: IAgentCharacter 停止
description: IAgentCharacter 停止
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372444"
---
# <a name="iagentcharacterstop"></a><span data-ttu-id="47920-103">IAgentCharacter：： Stop</span><span class="sxs-lookup"><span data-stu-id="47920-103">IAgentCharacter::Stop</span></span>

<span data-ttu-id="47920-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="47920-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

<span data-ttu-id="47920-105">停止指定的動畫 (要求) ，並將其從字元的動畫佇列中移除。</span><span class="sxs-lookup"><span data-stu-id="47920-105">Stops the specified animation (request) and removes it from the character's animation queue.</span></span>

-   <span data-ttu-id="47920-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="47920-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="47920-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="47920-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="47920-108">要停止的要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="47920-108">The ID of the request to stop.</span></span>

</dd> </dl>

<span data-ttu-id="47920-109">**停止** 也可以用來終止任何已排入佇列的 [**準備**](iagentcharacter--prepare.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="47920-109">**Stop** can also be used to halt any queued [**Prepare**](iagentcharacter--prepare.md) calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="47920-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47920-110">See Also</span></span>

<span data-ttu-id="47920-111">[**IAgentCharacter：:P 準備**](iagentcharacter--prepare.md)、 [ **IAgentCharacter：： StopAll**](iagentcharacter--stopall.md)</span><span class="sxs-lookup"><span data-stu-id="47920-111">[**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md)</span></span>


 

 




