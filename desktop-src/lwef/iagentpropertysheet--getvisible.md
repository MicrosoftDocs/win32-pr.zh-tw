---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301052"
---
# <a name="iagentpropertysheetgetvisible"></a><span data-ttu-id="1354d-103">IAgentPropertySheet：： GetVisible</span><span class="sxs-lookup"><span data-stu-id="1354d-103">IAgentPropertySheet::GetVisible</span></span>

<span data-ttu-id="1354d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="1354d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

<span data-ttu-id="1354d-105">判斷 Microsoft Agent 屬性工作表是否可見或隱藏。</span><span class="sxs-lookup"><span data-stu-id="1354d-105">Determines whether the Microsoft Agent property sheet is visible or hidden.</span></span>

-   <span data-ttu-id="1354d-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="1354d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="1354d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="1354d-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="1354d-108">如果屬性工作表是可見的，則為收到 **True** 的變數位址，如果隱藏，則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="1354d-108">Address of a variable that receives **True** if the property sheet is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="1354d-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1354d-109">See Also</span></span>

[<span data-ttu-id="1354d-110">**IAgentPropertySheet::SetVisible**</span><span class="sxs-lookup"><span data-stu-id="1354d-110">**IAgentPropertySheet::SetVisible**</span></span>](iagentpropertysheet--setvisible.md)


 

 




