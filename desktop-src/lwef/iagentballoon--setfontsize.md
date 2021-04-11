---
title: IAgentBalloon SetFontSize
description: IAgentBalloon SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311216"
---
# <a name="iagentballoonsetfontsize"></a><span data-ttu-id="79a8f-103">IAgentBalloon::SetFontSize</span><span class="sxs-lookup"><span data-stu-id="79a8f-103">IAgentBalloon::SetFontSize</span></span>

<span data-ttu-id="79a8f-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="79a8f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

<span data-ttu-id="79a8f-105">設定出現在文字提示字元中的字型大小。</span><span class="sxs-lookup"><span data-stu-id="79a8f-105">Sets the size of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="79a8f-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="79a8f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="79a8f-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="79a8f-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="79a8f-108">字型的大小。</span><span class="sxs-lookup"><span data-stu-id="79a8f-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="79a8f-109">在 [Microsoft 代理程式字元編輯器] 中，會定義字元字提示字元中使用的預設字型大小。</span><span class="sxs-lookup"><span data-stu-id="79a8f-109">The default font size used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="79a8f-110">您可以使用 **IAgentBalloon：： SetFontSize** 來變更它。</span><span class="sxs-lookup"><span data-stu-id="79a8f-110">You can change it with **IAgentBalloon::SetFontSize**.</span></span> <span data-ttu-id="79a8f-111">不過，使用者可以使用 Microsoft Agent 屬性工作表覆寫所有字元的字型大小設定。</span><span class="sxs-lookup"><span data-stu-id="79a8f-111">However, the user can override the font size setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="79a8f-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79a8f-112">See Also</span></span>

[<span data-ttu-id="79a8f-113">**IAgentBalloon::GetFontSize**</span><span class="sxs-lookup"><span data-stu-id="79a8f-113">**IAgentBalloon::GetFontSize**</span></span>](iagentballoon--getfontsize.md)


 

 




