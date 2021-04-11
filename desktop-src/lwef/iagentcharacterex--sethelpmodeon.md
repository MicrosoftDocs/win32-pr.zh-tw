---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092660"
---
# <a name="iagentcharacterexsethelpmodeon"></a><span data-ttu-id="15403-103">IAgentCharacterEx::SetHelpModeOn</span><span class="sxs-lookup"><span data-stu-id="15403-103">IAgentCharacterEx::SetHelpModeOn</span></span>

<span data-ttu-id="15403-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="15403-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

<span data-ttu-id="15403-105">為字元設定即時線上說明模式。</span><span class="sxs-lookup"><span data-stu-id="15403-105">Sets context-sensitive Help mode on for the character.</span></span>

-   <span data-ttu-id="15403-106">傳回 \_ [確定] 表示作業成功。</span><span class="sxs-lookup"><span data-stu-id="15403-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="15403-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span><span class="sxs-lookup"><span data-stu-id="15403-107"><span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*</span></span>
</dt> <dd>

<span data-ttu-id="15403-108">說明模式旗標。</span><span class="sxs-lookup"><span data-stu-id="15403-108">Help mode flag.</span></span> <span data-ttu-id="15403-109">如果此參數為 **True**，Microsoft Agent 會開啟字元的說明模式。</span><span class="sxs-lookup"><span data-stu-id="15403-109">If this parameter is **True**, Microsoft Agent turns on Help mode for the character.</span></span>

</dd> </dl>

<span data-ttu-id="15403-110">當您將這個屬性設定為 **True** 時，滑鼠指標會在移至字元上方或移至字元的快顯功能表時，變更為內容相關的說明影像。</span><span class="sxs-lookup"><span data-stu-id="15403-110">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="15403-111">當使用者按一下或拖曳字元，或在字元的快顯功能表中按一下專案時，伺服器會觸發 [**IAgentNotifySinkEx：： HelpComplete**](iagentnotifysinkex--helpcomplete.md) 事件並離開說明模式。</span><span class="sxs-lookup"><span data-stu-id="15403-111">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md) event and exits Help mode.</span></span>

<span data-ttu-id="15403-112">在 [說明] 模式中，除非 [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)屬性傳回 **True**，否則伺服器不會傳送 [**Click**](click-event.md)、 [**DragStart**](/windows/desktop/lwef/dragstart-event)、 [**DragComplete**](https://www.bing.com/search?q=**DragComplete**)和 [**命令**](command-event.md)事件。</span><span class="sxs-lookup"><span data-stu-id="15403-112">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](/windows/desktop/lwef/dragstart-event), [**DragComplete**](https://www.bing.com/search?q=**DragComplete**), and [**Command**](command-event.md) events, unless the [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) property returns **True**.</span></span> <span data-ttu-id="15403-113">在這種情況下，伺服器會傳送 **Click** 事件 (不會離開說明模式) ，而只是針對滑鼠右鍵，如此您就可以顯示快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="15403-113">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button so you can display the pop-up menu.</span></span>

<span data-ttu-id="15403-114">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="15403-114">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="15403-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15403-115">See Also</span></span>

<span data-ttu-id="15403-116">[**IAgentCharacterEx：： GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md)、 [ **IAgentNotifySinkEx：： HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="15403-116">[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [**IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)</span></span>


 

 