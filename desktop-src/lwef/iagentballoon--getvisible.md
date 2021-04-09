---
title: IAgentBalloon GetVisible
description: IAgentBalloon GetVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840759"
---
# <a name="iagentballoongetvisible"></a><span data-ttu-id="2a9c4-103">IAgentBalloon：： GetVisible</span><span class="sxs-lookup"><span data-stu-id="2a9c4-103">IAgentBalloon::GetVisible</span></span>

<span data-ttu-id="2a9c4-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2a9c4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

<span data-ttu-id="2a9c4-105">決定是否顯示或隱藏文字提示。</span><span class="sxs-lookup"><span data-stu-id="2a9c4-105">Determines whether the word balloon is visible or hidden.</span></span>

-   <span data-ttu-id="2a9c4-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="2a9c4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2a9c4-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="2a9c4-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="2a9c4-108">如果可以看到文字批註，則為收到 **True** 的變數位址，如果隱藏，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="2a9c4-108">Address of a variable that receives **True** if the word balloon is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2a9c4-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a9c4-109">See Also</span></span>

[<span data-ttu-id="2a9c4-110">**IAgentBalloon::SetVisible**</span><span class="sxs-lookup"><span data-stu-id="2a9c4-110">**IAgentBalloon::SetVisible**</span></span>](iagentballoon--setvisible.md)


 

 




