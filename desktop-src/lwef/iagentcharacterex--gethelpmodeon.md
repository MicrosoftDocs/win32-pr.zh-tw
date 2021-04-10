---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184015"
---
# <a name="iagentcharacterexgethelpmodeon"></a><span data-ttu-id="89738-103">IAgentCharacterEx::GetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="89738-103">IAgentCharacterEx::GetHelpModeOn</span></span>

<span data-ttu-id="89738-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="89738-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

<span data-ttu-id="89738-105">抓取是否為字元的即時線上說明模式。</span><span class="sxs-lookup"><span data-stu-id="89738-105">Retrieves whether context-sensitive Help mode is on for the character.</span></span>

-   <span data-ttu-id="89738-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="89738-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="89738-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="89738-107"><span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="89738-108">如果字元的說明模式為 on，則為收到 **True** 之變數的位址，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="89738-108">Address of a variable that receives **True** if Help mode is on for the character and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="89738-109">當這個屬性設定為 **True** 時，滑鼠指標會在移至字元上方或移至字元的快顯功能表時，變更為內容相關的說明影像。</span><span class="sxs-lookup"><span data-stu-id="89738-109">When this property is set to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="89738-110">當使用者按一下或拖曳字元，或在字元的快顯功能表中按一下專案時，伺服器會觸發 [**IAgentNotifySinkEx：： HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) 事件並離開說明模式。</span><span class="sxs-lookup"><span data-stu-id="89738-110">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) event and exits Help mode.</span></span>

<span data-ttu-id="89738-111">在 [說明] 模式中，除非 [**ragcomplete**](https://www.bing.com/search?q=**GetAutoPopupMenu**)屬性傳回 **True**，否則伺服器不會傳送 [**IAgentNotifySink：： Click**](iagentnotifysink--click.md)、 [**IAgentNotifySink：:D Ragstart**](iagentnotifysink--dragstart.md)、 [**IAgentNotifySink：:D IAgentNotifySink**](iagentnotifysink--dragcomplete.md)和 [**GetAutoPopupMenu：：命令**](iagentnotifysink--command.md)事件。</span><span class="sxs-lookup"><span data-stu-id="89738-111">In Help mode, the server does not send the [**IAgentNotifySink::Click**](iagentnotifysink--click.md), [**IAgentNotifySink::DragStart**](iagentnotifysink--dragstart.md), [**IAgentNotifySink::DragComplete**](iagentnotifysink--dragcomplete.md), and [**IAgentNotifySink::Command**](iagentnotifysink--command.md) events, unless [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) property returns **True**.</span></span> <span data-ttu-id="89738-112">在這種情況下，伺服器會傳送 **IAgentNotifySink：： Click** 事件 (不會離開說明模式) ，而只有滑鼠右鍵可讓您顯示快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="89738-112">In that case, the server will send the **IAgentNotifySink::Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="89738-113">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="89738-113">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="89738-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89738-114">See Also</span></span>

[<span data-ttu-id="89738-115">**IAgentCharacterEx::SetHelpModeOn**</span><span class="sxs-lookup"><span data-stu-id="89738-115">**IAgentCharacterEx::SetHelpModeOn**</span></span>](iagentcharacterex--sethelpmodeon.md)


 

 




