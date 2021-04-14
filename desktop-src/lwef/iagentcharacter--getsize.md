---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e40c219cd0a1dc1d11738149ca7cfd9869fe682e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311595"
---
# <a name="iagentcharactergetsize"></a><span data-ttu-id="0e350-103">IAgentCharacter：： GetSize</span><span class="sxs-lookup"><span data-stu-id="0e350-103">IAgentCharacter::GetSize</span></span>

<span data-ttu-id="0e350-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0e350-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

<span data-ttu-id="0e350-105">抓取字元動畫框架的大小。</span><span class="sxs-lookup"><span data-stu-id="0e350-105">Retrieves the size of the character's animation frame.</span></span>

-   <span data-ttu-id="0e350-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0e350-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0e350-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="0e350-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="0e350-108">接收字元動畫框架寬度的變數位址（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="0e350-108">Address of a variable that receives the width of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="0e350-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="0e350-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="0e350-110">接收字元動畫框架高度的變數位址（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="0e350-110">Address of a variable that receives the height of the character animation frame in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="0e350-111">雖然字元會出現在不規則形狀的區域視窗中，但字元的位置是以其矩形動畫框架為基礎。</span><span class="sxs-lookup"><span data-stu-id="0e350-111">Even though the character appears in an irregularly shaped region window, the location of the character is based on its rectangular animation frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="0e350-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0e350-112">See Also</span></span>

[<span data-ttu-id="0e350-113">**IAgentCharacter：： SetSize**</span><span class="sxs-lookup"><span data-stu-id="0e350-113">**IAgentCharacter::SetSize**</span></span>](iagentcharacter--setsize.md)


 

 




