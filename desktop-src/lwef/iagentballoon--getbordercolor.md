---
title: IAgentBalloon GetBorderColor
description: IAgentBalloon GetBorderColor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674231"
---
# <a name="iagentballoongetbordercolor"></a><span data-ttu-id="1e5dc-103">IAgentBalloon::GetBorderColor</span><span class="sxs-lookup"><span data-stu-id="1e5dc-103">IAgentBalloon::GetBorderColor</span></span>

<span data-ttu-id="1e5dc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1e5dc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

<span data-ttu-id="1e5dc-105">抓取針對文字氣球顯示之框線色彩的值。</span><span class="sxs-lookup"><span data-stu-id="1e5dc-105">Retrieves the value for the border color displayed for a word balloon.</span></span>

-   <span data-ttu-id="1e5dc-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1e5dc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1e5dc-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span><span class="sxs-lookup"><span data-stu-id="1e5dc-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span></span>
</dt> <dd>

<span data-ttu-id="1e5dc-108">接收氣球框線色彩設定之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="1e5dc-108">The address of a variable that receives the color setting for the balloon border.</span></span>

</dd> </dl>

<span data-ttu-id="1e5dc-109">字元文字氣球的框線色彩是在 Microsoft Agent 字元編輯器中定義。</span><span class="sxs-lookup"><span data-stu-id="1e5dc-109">The border color for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="1e5dc-110">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="1e5dc-110">It cannot be changed by an application.</span></span> <span data-ttu-id="1e5dc-111">不過，使用者可以透過 Microsoft Agent 屬性工作表變更所有字元之文字批註的框線色彩。</span><span class="sxs-lookup"><span data-stu-id="1e5dc-111">However, the user can change the border color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e5dc-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e5dc-112">See Also</span></span>

<span data-ttu-id="1e5dc-113">[**IAgentBalloon：： GetBackColor**](iagentballoon--getbackcolor.md)、 [ **IAgentBalloon：： GetForeColor**](iagentballoon--getforecolor.md)</span><span class="sxs-lookup"><span data-stu-id="1e5dc-113">[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)</span></span>


 

 




