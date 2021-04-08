---
title: IAgentCharacterEx GetAutoPopupMenu
description: IAgentCharacterEx GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932416"
---
# <a name="iagentcharacterexgetautopopupmenu"></a><span data-ttu-id="044ab-103">IAgentCharacterEx::GetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="044ab-103">IAgentCharacterEx::GetAutoPopupMenu</span></span>

<span data-ttu-id="044ab-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="044ab-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

<span data-ttu-id="044ab-105">抓取伺服器是否自動顯示字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="044ab-105">Retrieves whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="044ab-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="044ab-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="044ab-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="044ab-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="044ab-108">如果 Microsoft 代理程式伺服器自動處理顯示字元的快顯功能表，則為收到 **True** 之變數的位址，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="044ab-108">Address of a variable that receives **True** if the Microsoft Agent server automatically handles displaying the character's pop-up menu and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="044ab-109">當這個屬性設定為 **False** 時，您的應用程式必須使用 [**IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) 方法來顯示快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="044ab-109">When this property is set to **False**, your application must display the pop-up menu using [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

<span data-ttu-id="044ab-110">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="044ab-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="044ab-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="044ab-111">See Also</span></span>

<span data-ttu-id="044ab-112">[**IAgentCharacterEx：： SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)、 [ **IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="044ab-112">[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




