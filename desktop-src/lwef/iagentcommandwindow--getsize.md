---
title: IAgentCommandWindow GetSize
description: IAgentCommandWindow GetSize
ms.assetid: 24ad3b48-6557-4790-b9c4-2cf7df92fa7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53cf42d98f811905590209b6fed70b28a5728903
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106980267"
---
# <a name="iagentcommandwindowgetsize"></a><span data-ttu-id="de2db-103">IAgentCommandWindow：： GetSize</span><span class="sxs-lookup"><span data-stu-id="de2db-103">IAgentCommandWindow::GetSize</span></span>

<span data-ttu-id="de2db-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="de2db-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for Voice Commands Window width
   long * plHeight  // address of variable for Voice Commands Window height
);
```

<span data-ttu-id="de2db-105">抓取語音命令視窗的目前大小。</span><span class="sxs-lookup"><span data-stu-id="de2db-105">Retrieves the current size of the Voice Commands Window.</span></span>

-   <span data-ttu-id="de2db-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="de2db-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="de2db-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span><span class="sxs-lookup"><span data-stu-id="de2db-107"><span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*</span></span>
</dt> <dd>

<span data-ttu-id="de2db-108">以圖元為單位的變數位址，以圖元為單位來接收語音命令視窗的寬度， (左上) 。</span><span class="sxs-lookup"><span data-stu-id="de2db-108">Address of a variable that receives the width of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="de2db-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span><span class="sxs-lookup"><span data-stu-id="de2db-109"><span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*</span></span>
</dt> <dd>

<span data-ttu-id="de2db-110">以圖元為單位的變數位址，此變數會以圖元為單位來接收語音命令視窗的高度（相對於螢幕原點 (左上) ）。</span><span class="sxs-lookup"><span data-stu-id="de2db-110">Address of a variable that receives the height of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="de2db-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de2db-111">See Also</span></span>

[<span data-ttu-id="de2db-112">**IAgentCommandWindow：： GetPosition**</span><span class="sxs-lookup"><span data-stu-id="de2db-112">**IAgentCommandWindow::GetPosition**</span></span>](iagentcommandwindow--getposition.md)


 

 




