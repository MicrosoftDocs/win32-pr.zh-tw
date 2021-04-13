---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cdff0d6876fc7257e05014f3d9ba695db5d168
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311600"
---
# <a name="iagentcharactergetposition"></a><span data-ttu-id="4835c-103">IAgentCharacter：： GetPosition</span><span class="sxs-lookup"><span data-stu-id="4835c-103">IAgentCharacter::GetPosition</span></span>

<span data-ttu-id="4835c-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4835c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

<span data-ttu-id="4835c-105">抓取字元的動畫畫面格位置。</span><span class="sxs-lookup"><span data-stu-id="4835c-105">Retrieves the character's animation frame position.</span></span>

-   <span data-ttu-id="4835c-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="4835c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4835c-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="4835c-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="4835c-108">接收字元動畫框架左邊緣（以圖元為單位）之螢幕座標的變數位址，相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="4835c-108">Address of a variable that receives the screen coordinate of the character animation frame's left edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="4835c-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="4835c-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="4835c-110">以圖元為單位的變數位址，此變數會接收字元動畫框架頂端邊緣的螢幕座標（相對於螢幕原點 (左上) ）。</span><span class="sxs-lookup"><span data-stu-id="4835c-110">Address of a variable that receives the screen coordinate of the character animation frame's top edge in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="4835c-111">雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。</span><span class="sxs-lookup"><span data-stu-id="4835c-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="4835c-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4835c-112">See Also</span></span>

<span data-ttu-id="4835c-113">[**IAgentCharacter：： SetPosition**](iagentcharacter--setposition.md)、 [ **IAgentCharacter：： GetSize**](iagentcharacter--getsize.md)</span><span class="sxs-lookup"><span data-stu-id="4835c-113">[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)</span></span>


 

 




