---
title: 語音命令視窗
description: 語音命令視窗
ms.assetid: vs|msagent|~\guidlin_12gn.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c4ad0a1521e8dacc941ba5b2ce5f6c264c65a31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967259"
---
# <a name="voice-commands-window"></a><span data-ttu-id="9cbee-103">語音命令視窗</span><span class="sxs-lookup"><span data-stu-id="9cbee-103">Voice Commands Window</span></span>

<span data-ttu-id="9cbee-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="9cbee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="9cbee-105">[語音命令] 視窗會顯示字元目前可用的語音命令。</span><span class="sxs-lookup"><span data-stu-id="9cbee-105">The Voice Commands Window displays the current active voice commands available for the character.</span></span> <span data-ttu-id="9cbee-106">當您選擇 [開啟命令視窗] 命令或 [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object)物件的 [**Visible**](visible-property.md)屬性設定為 **True** 時，會出現此視窗。</span><span class="sxs-lookup"><span data-stu-id="9cbee-106">The window appears when the Open Commands Window command is chosen or the [**Visible**](visible-property.md) property of the [**CommandsWindow**](/windows/desktop/lwef/the-commandswindow-object) object is set to **True**.</span></span> <span data-ttu-id="9cbee-107">如果語音引擎尚未載入，則查詢或設定這個屬性會導致 Microsoft Agent 嘗試初始化引擎。</span><span class="sxs-lookup"><span data-stu-id="9cbee-107">If the speech engine has not yet been loaded, querying or setting this property will cause Microsoft Agent to attempt to initialize the engine.</span></span> <span data-ttu-id="9cbee-108">如果使用者停用語音，視窗仍然可以顯示;但是，它會包含文字訊息，通知使用者語音目前已停用。</span><span class="sxs-lookup"><span data-stu-id="9cbee-108">If the user disables speech, the window can still display; however, it will include a text message that informs the user that speech is currently disabled.</span></span>

<span data-ttu-id="9cbee-109">輸入-主動用戶端的命令會根據其 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 [**VoiceCaption**](voicecaption-property.md)下所列的 [**語音**](voice-property.md)[**字幕**](caption-property.md)和 **語音** 屬性設定，出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="9cbee-109">The input-active client's commands appear in the Voice Commands Window based on the [**Voice**](voice-property.md)[**Caption**](caption-property.md) and **Voice** property settings listed under the [**VoiceCaption**](voicecaption-property.md) of their [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

<span data-ttu-id="9cbee-110">**圖1。語音命令視窗**</span><span class="sxs-lookup"><span data-stu-id="9cbee-110">**Figure 1. Voice Commands Window**</span></span>

<span data-ttu-id="9cbee-111">選擇 [開啟命令視窗] 命令時，會出現 [語音命令] 視窗。</span><span class="sxs-lookup"><span data-stu-id="9cbee-111">The Voice Commands Window appears when the Open Commands Window command is chosen.</span></span> <span data-ttu-id="9cbee-112">輸入-主動用戶端的命令會根據 [[**命令**](/windows/desktop/lwef/the-commands-collection-object)集合的 **聲音**] 下所列的 [[**語音**](voice-property.md)[**] 和 [**](caption-property.md) **語音**] 屬性設定，出現在 [語音命令] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="9cbee-112">The input-active client's commands appear in the Voice Commands Window based on the [**Voice**](voice-property.md)[**Caption**](caption-property.md) and **Voice** property settings listed under **Voice** of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

<span data-ttu-id="9cbee-113">[語音命令] 視窗也會列出其他字元用戶端的 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合 [**VoiceCaption**](voicecaption-property.md) ，以及下列全域命令專案下一般互動的伺服器產生的語音命令：</span><span class="sxs-lookup"><span data-stu-id="9cbee-113">The Voice Commands Window also lists the [**VoiceCaption**](voicecaption-property.md) of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection for other clients of the character, and the following server-generated voice commands for general interaction under the Global Commands entry:</span></span>



| <span data-ttu-id="9cbee-114">語音標題</span><span class="sxs-lookup"><span data-stu-id="9cbee-114">Voice Caption</span></span>                       | <span data-ttu-id="9cbee-115">語音文法</span><span class="sxs-lookup"><span data-stu-id="9cbee-115">Voice Grammar</span></span>                                                                                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cbee-116">開啟 [ \| 關閉語音命令] 視窗</span><span class="sxs-lookup"><span data-stu-id="9cbee-116">Open \| Close Voice Commands Window</span></span> | <span data-ttu-id="9cbee-117"> (開啟 \| [顯示 \[ ]) [ \] 命令 \[ ] 視窗 \] \| 我現在可以說什麼 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cbee-117">(open \| show) \[the\] commands \[window\] \| what can I say \[now\]</span></span> <br/> <span data-ttu-id="9cbee-118">切換為：</span><span class="sxs-lookup"><span data-stu-id="9cbee-118">toggles with:</span></span> <br/> <span data-ttu-id="9cbee-119">關閉 \[ \] 命令 \[ 視窗\]</span><span class="sxs-lookup"><span data-stu-id="9cbee-119">close \[the\] commands \[window\]</span></span> <br/> |
| <span data-ttu-id="9cbee-120">隱藏</span><span class="sxs-lookup"><span data-stu-id="9cbee-120">Hide</span></span>                                | <span data-ttu-id="9cbee-121">隱藏 \*</span><span class="sxs-lookup"><span data-stu-id="9cbee-121">hide \*</span></span>                                                                                                                                                  |
| <span data-ttu-id="9cbee-122">*CharacterName*</span><span class="sxs-lookup"><span data-stu-id="9cbee-122">*CharacterName*</span></span>                     | <span data-ttu-id="9cbee-123">*CharacterName*\*\*</span><span class="sxs-lookup"><span data-stu-id="9cbee-123">*CharacterName*\*\*</span></span>                                                                                                                                      |
| <span data-ttu-id="9cbee-124">全域命令</span><span class="sxs-lookup"><span data-stu-id="9cbee-124">Global Commands</span></span>                     | <span data-ttu-id="9cbee-125">\[顯示 \] \[ \] 全域命令</span><span class="sxs-lookup"><span data-stu-id="9cbee-125">\[show\] \[me\] global commands</span></span>                                                                                                                          |



 

<span data-ttu-id="9cbee-126">\* 只有當字元目前可見時，才會列出該字元。</span><span class="sxs-lookup"><span data-stu-id="9cbee-126">\* A character is listed here only if it is currently visible.</span></span>

<span data-ttu-id="9cbee-127">\*\* 所有載入的字元都會列出。</span><span class="sxs-lookup"><span data-stu-id="9cbee-127">\*\* All loaded characters are listed.</span></span>

<span data-ttu-id="9cbee-128">說到另一個用戶端 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合的 voice 命令會切換到該用戶端，而 [語音命令] 視窗則會顯示該用戶端的命令。</span><span class="sxs-lookup"><span data-stu-id="9cbee-128">Speaking the voice command for another client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection switches to that client, and the Voice Commands Window displays the commands of that client.</span></span> <span data-ttu-id="9cbee-129">不會展開其他專案。</span><span class="sxs-lookup"><span data-stu-id="9cbee-129">No other entries are expanded.</span></span> <span data-ttu-id="9cbee-130">同樣地，如果使用者切換字元，[語音命令] 視窗就會變更，以顯示其輸入-主動用戶端的命令。</span><span class="sxs-lookup"><span data-stu-id="9cbee-130">Similarly, if the user switches characters, the Voice Commands Window changes to display the commands of its input-active client.</span></span> <span data-ttu-id="9cbee-131">如果用戶端已經輸入-主動，說出其中一個語音命令沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9cbee-131">If the client is already input-active, speaking one of its voice commands has no effect.</span></span> <span data-ttu-id="9cbee-132"> (不過，如果使用者使用滑鼠來折迭作用中用戶端的子樹狀結構，則說出用戶端名稱會重新出現用戶端的子樹。 ) </span><span class="sxs-lookup"><span data-stu-id="9cbee-132">(However, if the user collapses the active client's subtree with the mouse, speaking the client name redisplays the client's subtree.)</span></span>

<span data-ttu-id="9cbee-133">如果用戶端有語音命令，但沒有 [**命令**](/windows/desktop/lwef/the-commands-collection-object)物件的 [**聲音**](voice-property.md)設定 (或沒有 **語音**[**標題**](caption-property.md)) ，則樹狀結構會顯示「 (命令未定義) 」作為父專案--但只有在該用戶端為輸入-主動且用戶端在其集合中具有 **標題** 和 **語音** 設定的命令時才會顯示。</span><span class="sxs-lookup"><span data-stu-id="9cbee-133">If a client has voice commands, but no [**Voice**](voice-property.md) setting for its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object (or no **Voice**[**Caption**](caption-property.md)), the tree displays "(command undefined)" as the parent entry -- but only when that client is input-active and the client has commands in its collection that have **Caption** and **Voice** settings.</span></span>

<span data-ttu-id="9cbee-134">伺服器會自動顯示目前輸入-主動用戶端的命令，並視需要滾動視窗，以根據視窗的大小，盡可能顯示用戶端的命令數目。</span><span class="sxs-lookup"><span data-stu-id="9cbee-134">The server automatically displays the commands of the current input-active client and, if necessary, scrolls the window to display as many of the client's commands as possible, based on the size of the window.</span></span> <span data-ttu-id="9cbee-135">如果字元沒有用戶端專案，則會展開全域命令專案。</span><span class="sxs-lookup"><span data-stu-id="9cbee-135">If the character has no client entries, the Global Commands entry is expanded.</span></span>

<span data-ttu-id="9cbee-136">如果使用者說「全域命令」，[語音命令] 視窗一律會顯示其相關聯的子樹狀目錄專案。</span><span class="sxs-lookup"><span data-stu-id="9cbee-136">If the user speaks "Global Commands," the Voice Commands Window always displays its associated subtree entries.</span></span> <span data-ttu-id="9cbee-137">如果已顯示，則命令沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="9cbee-137">If they are already displayed, the command has no effect.</span></span>

<span data-ttu-id="9cbee-138">雖然您也可以使用 [**Visible**](visible-property.md) 屬性，從應用程式的程式碼顯示或隱藏 [語音命令] 視窗，但無法變更語音命令視窗大小或位置。</span><span class="sxs-lookup"><span data-stu-id="9cbee-138">Although you can also display or hide the Voice Commands Window from your application's code using the [**Visible**](visible-property.md) property, you cannot change the Voice Commands Window size or location.</span></span> <span data-ttu-id="9cbee-139">伺服器會根據使用者與視窗的互動，來維護 [語音命令] 視窗的屬性。</span><span class="sxs-lookup"><span data-stu-id="9cbee-139">The server maintains the Voice Commands Window's properties based on the user's interaction with the window.</span></span> <span data-ttu-id="9cbee-140">它的初始位置會緊接在字元的工作列圖示的旁邊。</span><span class="sxs-lookup"><span data-stu-id="9cbee-140">Its initial location is immediately adjacent to the character's taskbar icon.</span></span>

<span data-ttu-id="9cbee-141">[語音命令] 視窗會包含在 ALT + TAB 視窗順序中。</span><span class="sxs-lookup"><span data-stu-id="9cbee-141">The Voice Commands Window is included in the ALT+TAB window order.</span></span> <span data-ttu-id="9cbee-142">這可讓使用者切換至視窗，以使用鍵盤來滾動、調整大小或重新調整視窗的大小。</span><span class="sxs-lookup"><span data-stu-id="9cbee-142">This enables a user to switch to the window to scroll, resize, or reposition the window with the keyboard.</span></span>

-   [<span data-ttu-id="9cbee-143">接聽秘訣</span><span class="sxs-lookup"><span data-stu-id="9cbee-143">The Listening Tip</span></span>](the-listening-tip.md)
-   <span data-ttu-id="9cbee-144">[[先進的字元選項] 視窗](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)</span><span class="sxs-lookup"><span data-stu-id="9cbee-144">[The Advanced Character Options Window](https://www.bing.com/search?q=The+Advanced+Character+Options+Window)</span></span>

 

