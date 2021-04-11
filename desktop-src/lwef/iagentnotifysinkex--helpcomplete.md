---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023348"
---
# <a name="iagentnotifysinkexhelpcomplete"></a><span data-ttu-id="6cfcc-103">IAgentNotifySinkEx::HelpComplete</span><span class="sxs-lookup"><span data-stu-id="6cfcc-103">IAgentNotifySinkEx::HelpComplete</span></span>

<span data-ttu-id="6cfcc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="6cfcc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

<span data-ttu-id="6cfcc-105">當使用者選取命令或字元來完成說明模式時，通知用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-105">Notifies a client application when the user selects a command or character to complete Help mode.</span></span>

-   <span data-ttu-id="6cfcc-106">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="6cfcc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="6cfcc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="6cfcc-108">說明模式完成之字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-108">Identifier of the character for which Help mode completed.</span></span>

</dd> <dt>

<span data-ttu-id="6cfcc-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="6cfcc-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="6cfcc-110">使用者選取之命令的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-110">Identifier of the command the user selected.</span></span>

</dd> <dt>

<span data-ttu-id="6cfcc-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="6cfcc-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="6cfcc-112">事件的原因可能是下列值：</span><span class="sxs-lookup"><span data-stu-id="6cfcc-112">The cause for the event, which may be the following values:</span></span>



| <span data-ttu-id="6cfcc-113">值</span><span class="sxs-lookup"><span data-stu-id="6cfcc-113">Value</span></span>                                                                         | <span data-ttu-id="6cfcc-114">描述</span><span class="sxs-lookup"><span data-stu-id="6cfcc-114">Description</span></span>                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfcc-115">**const 不帶正負號的 short** **CSHELPCAUSE \_ 命令 = 1;**</span><span class="sxs-lookup"><span data-stu-id="6cfcc-115">**const unsigned short** **CSHELPCAUSE\_COMMAND = 1;**</span></span><br/>             | <span data-ttu-id="6cfcc-116">使用者選取了您的應用程式所提供的命令。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-116">The user selected a command supplied by your application.</span></span>                            |
| <span data-ttu-id="6cfcc-117">**const 不帶正負號的 short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**</span><span class="sxs-lookup"><span data-stu-id="6cfcc-117">**const unsigned short** **CSHELPCAUSE\_OTHERPROGRAM = 2;**</span></span><br/>        | <span data-ttu-id="6cfcc-118">使用者選取了另一個用戶端的 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-118">The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span> |
| <span data-ttu-id="6cfcc-119">**const 不帶正負號的 short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**</span><span class="sxs-lookup"><span data-stu-id="6cfcc-119">**const unsigned short** **CSHELPCAUSE\_OPENCOMMANDSWINDOW = 3;**</span></span><br/>  | <span data-ttu-id="6cfcc-120">使用者選取了 [開啟語音命令] 命令。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-120">The user selected the Open Voice Commands command.</span></span>                                   |
| <span data-ttu-id="6cfcc-121">**const 不帶正負號的 short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**</span><span class="sxs-lookup"><span data-stu-id="6cfcc-121">**const unsigned short** **CSHELPCAUSE\_CLOSECOMMANDSWINDOW = 4;**</span></span><br/> | <span data-ttu-id="6cfcc-122">使用者選取了 [關閉語音命令] 命令。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-122">The user selected the Close Voice Commands command.</span></span>                                  |
| <span data-ttu-id="6cfcc-123">**const 不帶正負號的 short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**</span><span class="sxs-lookup"><span data-stu-id="6cfcc-123">**const unsigned short** **CSHELPCAUSE\_SHOWCHARACTER = 5;**</span></span><br/>       | <span data-ttu-id="6cfcc-124">使用者已選取 [顯示 *CharacterName* ] 命令。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-124">The user selected the Show *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="6cfcc-125">**const 不帶正負號的 short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**</span><span class="sxs-lookup"><span data-stu-id="6cfcc-125">**const unsigned short** **CSHELPCAUSE\_HIDECHARACTER = 6;**</span></span><br/>       | <span data-ttu-id="6cfcc-126">使用者選取了 [隱藏 *CharacterName* ] 命令。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-126">The user selected the Hide *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="6cfcc-127">**const 不帶正負號的短** **CSHELPCAUSE \_ 字元 = 7;**</span><span class="sxs-lookup"><span data-stu-id="6cfcc-127">**const unsigned short** **CSHELPCAUSE\_CHARACTER = 7;**</span></span><br/>           | <span data-ttu-id="6cfcc-128">選取的使用者 (按一下) 字元。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-128">The user selected (clicked) the character.</span></span>                                           |



 

</dd> </dl>

<span data-ttu-id="6cfcc-129">當使用者按一下或拖曳字元，或從字元的快顯功能表中選取命令時，[說明] 模式通常會完成。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-129">Typically Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="6cfcc-130">按一下其他字元或螢幕上的其他位置，並不會取消說明模式。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-130">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="6cfcc-131">設定字元說明模式的用戶端可以將 [**IAgentCharacter：： HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) 設定為 **False**，以取消說明模式。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-131">The client that set Help mode for the character can cancel Help mode by setting [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) to **False**.</span></span> <span data-ttu-id="6cfcc-132"> (這不會觸發 **IAgentNotifySinkEx：： HelpComplete** 事件。 ) </span><span class="sxs-lookup"><span data-stu-id="6cfcc-132">(This does not trigger the **IAgentNotifySinkEx::HelpComplete** event.)</span></span>

<span data-ttu-id="6cfcc-133">當使用者從 [說明] 模式中的字元快顯功能表選取命令時，伺服器會移除功能表、使用 [**命令指定的**](helpcontextid-property.md)協助工具來呼叫說明，並傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-133">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="6cfcc-134">與內容相關的 (也稱為「這是什麼？ ) 說明視窗會顯示在指標位置。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-134">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="6cfcc-135">如果使用者選取語音輸入的命令，則會在字元上顯示 [說明] 視窗。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-135">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="6cfcc-136">如果字元是在螢幕上，視窗會在畫面上顯示最接近字元的目前位置。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-136">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="6cfcc-137">如果伺服器以空字串的形式傳回 *dwCommandID* ( "" ) ，表示使用者已選取伺服器提供的命令。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-137">If the server returns *dwCommandID* as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="6cfcc-138">此事件只會傳送至用戶端應用程式，以將字元放入說明模式。</span><span class="sxs-lookup"><span data-stu-id="6cfcc-138">This event is sent only to the client application that places the character into Help mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cfcc-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cfcc-139">See Also</span></span>

<span data-ttu-id="6cfcc-140">[**IAgentCharacterEx：： SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)、 [**IAgentCharacterEx：： SetHelpFileName**](iagentcharacterex--sethelpfilename.md)、 [**IAgentCharacterEx：： SetHelpCoNtextID**](iagentcharacterex--sethelpcontextid.md)、 [**IAgentCommandsEx：： SetHelpCoNtextID**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="6cfcc-140">[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>


 

