---
title: IAgentCharacterEx GetOriginalSize
description: IAgentCharacterEx GetOriginalSize
ms.assetid: a27ae88f-3655-4375-b563-0cc320d012cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e1712587e70d9756e3d37ca9e0f3cbfdb82c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021264"
---
# <a name="iagentcharacterexgetoriginalsize"></a><span data-ttu-id="10e41-103">IAgentCharacterEx::GetOriginalSize</span><span class="sxs-lookup"><span data-stu-id="10e41-103">IAgentCharacterEx::GetOriginalSize</span></span>

<span data-ttu-id="10e41-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="10e41-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetOriginalSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="10e41-105">抓取字元動畫框架的原始大小。</span><span class="sxs-lookup"><span data-stu-id="10e41-105">Retrieves the original size of the character's animation frame.</span></span>

-   <span data-ttu-id="10e41-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="10e41-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="10e41-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="10e41-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="10e41-108">接收字元動畫框架原始寬度的變數位址（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="10e41-108">Address of a variable that receives the original width of the character animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="10e41-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="10e41-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="10e41-110">接收字元動畫框架原始高度的變數位址（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="10e41-110">Address of a variable that receives the original height of the character animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="10e41-111">此呼叫會傳回內建于 Microsoft Agent 字元編輯器中之字元框架的原始大小。</span><span class="sxs-lookup"><span data-stu-id="10e41-111">This call returns the original size of the character frame as built in the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="10e41-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10e41-112">See Also</span></span>

[<span data-ttu-id="10e41-113">**IAgentCharacter：： GetSize**</span><span class="sxs-lookup"><span data-stu-id="10e41-113">**IAgentCharacter::GetSize**</span></span>](iagentcharacter--getsize.md)


 

 




