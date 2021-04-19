---
title: IAgentPropertySheet GetSize
description: IAgentPropertySheet GetSize
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966802"
---
# <a name="iagentpropertysheetgetsize"></a><span data-ttu-id="f12cb-103">IAgentPropertySheet：： GetSize</span><span class="sxs-lookup"><span data-stu-id="f12cb-103">IAgentPropertySheet::GetSize</span></span>

<span data-ttu-id="f12cb-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f12cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

<span data-ttu-id="f12cb-105">抓取 Microsoft Agent 屬性工作表視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="f12cb-105">Retrieves the size of the Microsoft Agent property sheet window.</span></span>

-   <span data-ttu-id="f12cb-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="f12cb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f12cb-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="f12cb-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="f12cb-108">接收屬性工作表寬度的變數位址（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="f12cb-108">Address of a variable that receives the width of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="f12cb-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="f12cb-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="f12cb-110">以圖元為單位的變數位址，此變數會接收屬性工作表的高度（以圖元為單位），相對於螢幕原點 (左上角) 。</span><span class="sxs-lookup"><span data-stu-id="f12cb-110">Address of a variable that receives the height of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="f12cb-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f12cb-111">See Also</span></span>

[<span data-ttu-id="f12cb-112">**IAgentPropertySheet：： GetPosition**</span><span class="sxs-lookup"><span data-stu-id="f12cb-112">**IAgentPropertySheet::GetPosition**</span></span>](iagentpropertysheet--getposition.md)


 

 




