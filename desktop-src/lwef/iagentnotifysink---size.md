---
title: IAgentNotifySink 大小
description: IAgentNotifySink 大小
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507328"
---
# <a name="iagentnotifysinksize"></a><span data-ttu-id="b4332-103">IAgentNotifySink：： Size</span><span class="sxs-lookup"><span data-stu-id="b4332-103">IAgentNotifySink::Size</span></span>

<span data-ttu-id="b4332-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="b4332-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

<span data-ttu-id="b4332-105">當字元已調整大小時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="b4332-105">Notifies a client application when the character has been resized.</span></span>

-   <span data-ttu-id="b4332-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="b4332-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b4332-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="b4332-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="b4332-108">已調整大小之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b4332-108">Identifier of the character that has been resized.</span></span>

</dd> <dt>

<span data-ttu-id="b4332-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="b4332-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="b4332-110">字元動畫框架的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b4332-110">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="b4332-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="b4332-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="b4332-112">字元動畫框架的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b4332-112">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="b4332-113">此事件會傳送到字元的所有用戶端。</span><span class="sxs-lookup"><span data-stu-id="b4332-113">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4332-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4332-114">See Also</span></span>

<span data-ttu-id="b4332-115">[**IAgentCharacter：： GetSize**](iagentcharacter--getsize.md)、 [ **IAgentCharacter：： SetSize**](iagentcharacter--setsize.md)</span><span class="sxs-lookup"><span data-stu-id="b4332-115">[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md), [**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)</span></span>


 

 




