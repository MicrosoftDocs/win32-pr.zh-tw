---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932272"
---
# <a name="iagentcharacterexsetautopopupmenu"></a><span data-ttu-id="d3b5d-103">IAgentCharacterEx::SetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="d3b5d-103">IAgentCharacterEx::SetAutoPopupMenu</span></span>

<span data-ttu-id="d3b5d-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d3b5d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

<span data-ttu-id="d3b5d-105">設定伺服器是否自動顯示字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="d3b5d-105">Sets whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="d3b5d-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="d3b5d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d3b5d-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span><span class="sxs-lookup"><span data-stu-id="d3b5d-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="d3b5d-108">自動快顯功能表顯示旗標。</span><span class="sxs-lookup"><span data-stu-id="d3b5d-108">The automatic pop-up menu display flag.</span></span> <span data-ttu-id="d3b5d-109">如果此參數為 **True**，當使用者以滑鼠右鍵按一下字元或字元的工作列圖示時，Microsoft Agent 會自動顯示該字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="d3b5d-109">If this parameter is **True**, Microsoft Agent automatically displays the character's pop-up menu when the user right-clicks the character or character's taskbar icon.</span></span>

</dd> </dl>

<span data-ttu-id="d3b5d-110">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="d3b5d-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="d3b5d-111">藉由將這個屬性設定為 **False**，您就可以建立自己的功能表處理行為。</span><span class="sxs-lookup"><span data-stu-id="d3b5d-111">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="d3b5d-112">若要在將這個屬性設定為 **False** 之後顯示功能表，請使用 [**IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d3b5d-112">To display the menu after setting this property to **False**, use the [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3b5d-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3b5d-113">See Also</span></span>

<span data-ttu-id="d3b5d-114">[**IAgentCharacterEx：： GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)、 [ **IAgentCharacterEx：： ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="d3b5d-114">[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




