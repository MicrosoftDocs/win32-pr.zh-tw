---
title: IAgentBalloon GetForeColor
description: IAgentBalloon GetForeColor
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968255"
---
# <a name="iagentballoongetforecolor"></a><span data-ttu-id="f7cf3-103">IAgentBalloon::GetForeColor</span><span class="sxs-lookup"><span data-stu-id="f7cf3-103">IAgentBalloon::GetForeColor</span></span>

<span data-ttu-id="f7cf3-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="f7cf3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

<span data-ttu-id="f7cf3-105">抓取文字氣球中顯示之前景色彩的值。</span><span class="sxs-lookup"><span data-stu-id="f7cf3-105">Retrieves the value for the foreground color displayed in a word balloon.</span></span>

-   <span data-ttu-id="f7cf3-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="f7cf3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f7cf3-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span><span class="sxs-lookup"><span data-stu-id="f7cf3-107"><span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*</span></span>
</dt> <dd>

<span data-ttu-id="f7cf3-108">接收氣球前景色彩設定之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="f7cf3-108">The address of a variable that receives the color setting for the balloon foreground.</span></span>

</dd> </dl>

<span data-ttu-id="f7cf3-109">在「Microsoft 代理程式字元編輯器」中定義字元字提示字元中使用的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="f7cf3-109">The foreground color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="f7cf3-110">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="f7cf3-110">It cannot be changed by an application.</span></span> <span data-ttu-id="f7cf3-111">不過，使用者可以透過 Microsoft Agent 屬性工作表覆寫所有字元之文字批註的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="f7cf3-111">However, the user can override the foreground color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7cf3-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7cf3-112">See Also</span></span>

[<span data-ttu-id="f7cf3-113">**IAgentBalloon::GetBackColor**</span><span class="sxs-lookup"><span data-stu-id="f7cf3-113">**IAgentBalloon::GetBackColor**</span></span>](iagentballoon--getbackcolor.md)


 

 




