---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932300"
---
# <a name="iagentcommandwindowgetposition"></a><span data-ttu-id="1a7f9-103">IAgentCommandWindow：： GetPosition</span><span class="sxs-lookup"><span data-stu-id="1a7f9-103">IAgentCommandWindow::GetPosition</span></span>

<span data-ttu-id="1a7f9-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1a7f9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

<span data-ttu-id="1a7f9-105">抓取語音命令視窗的位置。</span><span class="sxs-lookup"><span data-stu-id="1a7f9-105">Retrieves the Voice Commands Window's position.</span></span>

-   <span data-ttu-id="1a7f9-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1a7f9-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1a7f9-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span><span class="sxs-lookup"><span data-stu-id="1a7f9-107"><span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*</span></span>
</dt> <dd>

<span data-ttu-id="1a7f9-108">變數的位址，此變數會接收 [語音命令] 視窗左邊緣的螢幕座標（單位為圖元），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="1a7f9-108">Address of a variable that receives the screen coordinate of the left edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="1a7f9-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span><span class="sxs-lookup"><span data-stu-id="1a7f9-109"><span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*</span></span>
</dt> <dd>

<span data-ttu-id="1a7f9-110">以圖元為單位的變數位址，此變數會接收 [語音命令] 視窗上邊緣的螢幕座標（以圖元為單位），相對於螢幕原點 (左上角) 。</span><span class="sxs-lookup"><span data-stu-id="1a7f9-110">Address of a variable that receives the screen coordinate of the top edge of the Voice Commands Window in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1a7f9-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1a7f9-111">See Also</span></span>

[<span data-ttu-id="1a7f9-112">**IAgentCommandWindow：： GetSize**</span><span class="sxs-lookup"><span data-stu-id="1a7f9-112">**IAgentCommandWindow::GetSize**</span></span>](iagentcommandwindow--getsize.md)


 

 




