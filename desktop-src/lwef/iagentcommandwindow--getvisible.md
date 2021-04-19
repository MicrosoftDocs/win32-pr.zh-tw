---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996147"
---
# <a name="iagentcommandwindowgetvisible"></a><span data-ttu-id="68516-103">IAgentCommandWindow：： GetVisible</span><span class="sxs-lookup"><span data-stu-id="68516-103">IAgentCommandWindow::GetVisible</span></span>

<span data-ttu-id="68516-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="68516-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

<span data-ttu-id="68516-105">決定是否顯示或隱藏 [語音命令] 視窗。</span><span class="sxs-lookup"><span data-stu-id="68516-105">Determines whether the Voice Commands Window is visible or hidden.</span></span>

-   <span data-ttu-id="68516-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="68516-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="68516-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="68516-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="68516-108">如果 [語音命令] 視窗是可見的，則為收到 **True** 的變數位址; 如果隱藏，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="68516-108">Address of a variable that receives **True** if the Voice Commands Window is visible, or **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="68516-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68516-109">See Also</span></span>

[<span data-ttu-id="68516-110">**IAgentCommandWindow::SetVisible**</span><span class="sxs-lookup"><span data-stu-id="68516-110">**IAgentCommandWindow::SetVisible**</span></span>](iagentcommandwindow--setvisible.md)


 

 




