---
title: IAgentCharacterEx ShowPopupMenu
description: IAgentCharacterEx ShowPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840363"
---
# <a name="iagentcharacterexshowpopupmenu"></a><span data-ttu-id="2c254-103">IAgentCharacterEx::ShowPopupMenu</span><span class="sxs-lookup"><span data-stu-id="2c254-103">IAgentCharacterEx::ShowPopupMenu</span></span>

<span data-ttu-id="2c254-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2c254-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

<span data-ttu-id="2c254-105">顯示字元的快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="2c254-105">Displays the pop-up menu for the character.</span></span>

-   <span data-ttu-id="2c254-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="2c254-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2c254-107"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="2c254-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="2c254-108">字元之快顯功能表的 x 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="2c254-108">The x-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="2c254-109"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="2c254-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="2c254-110">字元快顯功能表的 y 座標（以圖元為單位），相對於螢幕原點 (左上) 。</span><span class="sxs-lookup"><span data-stu-id="2c254-110">The y-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="2c254-111">當您將 [**IAgentCharacterEx：： SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) 設定為 **False** 時，當您以滑鼠右鍵按一下該字元或其工作列圖示時，伺服器就不會再自動顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="2c254-111">When you set [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) to **False**, the server no longer automatically displays the menu when the character or its taskbar icon is right-clicked.</span></span> <span data-ttu-id="2c254-112">您可以使用這個方法來顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="2c254-112">You can use this method to display the menu.</span></span>

<span data-ttu-id="2c254-113">功能表會顯示，直到使用者選取命令或顯示其他功能表為止。</span><span class="sxs-lookup"><span data-stu-id="2c254-113">The menu displays until the user selects a command or displays another menu.</span></span> <span data-ttu-id="2c254-114">一次只能顯示一個快顯功能表;因此，對此方法的呼叫將會取消 (移除) 前一個功能表中。</span><span class="sxs-lookup"><span data-stu-id="2c254-114">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="2c254-115">只有當您的用戶端應用程式是字元的作用中用戶端時，才會呼叫這個方法。否則會失敗。</span><span class="sxs-lookup"><span data-stu-id="2c254-115">This method should only be called when your client application is the active client of the character; otherwise it fails.</span></span>

[<span data-ttu-id="2c254-116">**IAgentCharacterEx::SetAutoPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="2c254-116">**IAgentCharacterEx::SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)

 

 




