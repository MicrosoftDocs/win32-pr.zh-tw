---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021646"
---
# <a name="iagentballoongetbackcolor"></a><span data-ttu-id="fd627-103">IAgentBalloon::GetBackColor</span><span class="sxs-lookup"><span data-stu-id="fd627-103">IAgentBalloon::GetBackColor</span></span>

<span data-ttu-id="fd627-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="fd627-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

<span data-ttu-id="fd627-105">抓取文字氣球中顯示之背景色彩的值。</span><span class="sxs-lookup"><span data-stu-id="fd627-105">Retrieves the value for the background color displayed in a word balloon.</span></span>

-   <span data-ttu-id="fd627-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="fd627-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fd627-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span><span class="sxs-lookup"><span data-stu-id="fd627-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span></span>
</dt> <dd>

<span data-ttu-id="fd627-108">接收球標背景之色彩設定的變數位址。</span><span class="sxs-lookup"><span data-stu-id="fd627-108">The address of a variable that receives the color setting for the balloon background.</span></span>

</dd> </dl>

<span data-ttu-id="fd627-109">在「Microsoft 代理程式字元編輯器」中定義字元字提示字元中所使用的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="fd627-109">The background color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="fd627-110">應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="fd627-110">It cannot be changed by an application.</span></span> <span data-ttu-id="fd627-111">不過，使用者可以透過 Microsoft Agent 屬性工作表變更所有字元的文字球的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="fd627-111">However, the user can change the background color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd627-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd627-112">See Also</span></span>

[<span data-ttu-id="fd627-113">**IAgentBalloon::GetForeColor**</span><span class="sxs-lookup"><span data-stu-id="fd627-113">**IAgentBalloon::GetForeColor**</span></span>](iagentballoon--getforecolor.md)


 

 




