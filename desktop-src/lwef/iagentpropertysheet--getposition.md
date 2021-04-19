---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968846"
---
# <a name="iagentpropertysheetgetposition"></a><span data-ttu-id="19aec-103">IAgentPropertySheet：： GetPosition</span><span class="sxs-lookup"><span data-stu-id="19aec-103">IAgentPropertySheet::GetPosition</span></span>

<span data-ttu-id="19aec-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="19aec-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

<span data-ttu-id="19aec-105">抓取 Microsoft 代理程式的屬性工作表視窗位置。</span><span class="sxs-lookup"><span data-stu-id="19aec-105">Retrieves the Microsoft Agent's property sheet window position.</span></span>

-   <span data-ttu-id="19aec-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="19aec-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="19aec-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="19aec-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="19aec-108">以圖元為單位的變數位址，此變數會接收屬性工作表左邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上角) 。</span><span class="sxs-lookup"><span data-stu-id="19aec-108">Address of a variable that receives the screen coordinate of the left edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="19aec-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="19aec-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="19aec-110">以圖元為單位的變數位址，此變數會接收屬性工作表上邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上角) 。</span><span class="sxs-lookup"><span data-stu-id="19aec-110">Address of a variable that receives the screen coordinate of the top edge of the property sheet in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="19aec-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19aec-111">See Also</span></span>

[<span data-ttu-id="19aec-112">**IAgentPropertySheet：： GetSize**</span><span class="sxs-lookup"><span data-stu-id="19aec-112">**IAgentPropertySheet::GetSize**</span></span>](iagentpropertysheet--getsize.md)


 

 




