---
title: IAgentBalloon SetVisible
description: IAgentBalloon SetVisible
ms.assetid: 682ebc6a-522d-4a39-bfa4-30a7c4d84d25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838c34397bc089ea49579b5f6a8c7d5834c8a580
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965371"
---
# <a name="iagentballoonsetvisible"></a><span data-ttu-id="0f566-103">IAgentBalloon::SetVisible</span><span class="sxs-lookup"><span data-stu-id="0f566-103">IAgentBalloon::SetVisible</span></span>

<span data-ttu-id="0f566-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="0f566-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // word balloon Visible setting 
);
```

<span data-ttu-id="0f566-105">設定文字氣球的 [**Visible**](visible-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="0f566-105">Sets the [**Visible**](visible-property.md) property for the word balloon.</span></span>

-   <span data-ttu-id="0f566-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="0f566-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="0f566-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="0f566-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="0f566-108">可見的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="0f566-108">Visible property setting.</span></span> <span data-ttu-id="0f566-109">值為 **True** 時，會顯示文字提示; **False** 值會將它隱藏。</span><span class="sxs-lookup"><span data-stu-id="0f566-109">A value of **True** displays the word balloon; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="0f566-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f566-110">See Also</span></span>

[<span data-ttu-id="0f566-111">**IAgentBalloon：： GetVisible**</span><span class="sxs-lookup"><span data-stu-id="0f566-111">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




