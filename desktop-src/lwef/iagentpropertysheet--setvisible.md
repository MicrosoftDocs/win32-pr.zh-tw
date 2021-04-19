---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968038"
---
# <a name="iagentpropertysheetsetvisible"></a><span data-ttu-id="49a57-103">IAgentPropertySheet::SetVisible</span><span class="sxs-lookup"><span data-stu-id="49a57-103">IAgentPropertySheet::SetVisible</span></span>

<span data-ttu-id="49a57-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="49a57-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

<span data-ttu-id="49a57-105">設定 Microsoft Agent 屬性工作表的 [**Visible**](visible-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="49a57-105">Sets the [**Visible**](visible-property.md) property for the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="49a57-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="49a57-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="49a57-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="49a57-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="49a57-108">可見的屬性設定。</span><span class="sxs-lookup"><span data-stu-id="49a57-108">Visible property setting.</span></span> <span data-ttu-id="49a57-109">值為 **True** 會顯示內容表; **False** 值會將它隱藏。</span><span class="sxs-lookup"><span data-stu-id="49a57-109">A value of **True** displays the property sheet; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="49a57-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49a57-110">See Also</span></span>

[<span data-ttu-id="49a57-111">**IAgentPropertySheet：： GetVisible**</span><span class="sxs-lookup"><span data-stu-id="49a57-111">**IAgentPropertySheet::GetVisible**</span></span>](iagentpropertysheet--getvisible.md)


 

 




