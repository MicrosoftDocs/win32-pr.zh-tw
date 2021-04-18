---
title: HelpComplete 事件
description: HelpComplete 事件
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965839"
---
# <a name="helpcomplete-event"></a><span data-ttu-id="3f409-103">HelpComplete 事件</span><span class="sxs-lookup"><span data-stu-id="3f409-103">HelpComplete Event</span></span>

<span data-ttu-id="3f409-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="3f409-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="3f409-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="3f409-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3f409-106">指出已結束內容相關的說明模式。</span><span class="sxs-lookup"><span data-stu-id="3f409-106">Indicates that context-sensitive Help mode has been exited.</span></span>

</dd> <dt>

<span data-ttu-id="3f409-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="3f409-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="3f409-108">\**子\*\*\*代理程式。 \* \* \* (byval* \*  \*CharacterID \* \* *，byval* \*  *名稱 \* \* *，byval* \*  *原因 \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="3f409-108">**Sub** *agent.\*\*\*(ByVal*\* *CharacterID\*\*\*, ByVal*\* *Name\*\*\*, ByVal*\* *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="3f409-109">部分</span><span class="sxs-lookup"><span data-stu-id="3f409-109">Part</span></span>          | <span data-ttu-id="3f409-110">描述</span><span class="sxs-lookup"><span data-stu-id="3f409-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f409-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="3f409-111">*CharacterID*</span></span> | <span data-ttu-id="3f409-112">以字串形式傳回已按下字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f409-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3f409-113">*名稱*</span><span class="sxs-lookup"><span data-stu-id="3f409-113">*Name*</span></span>        | <span data-ttu-id="3f409-114">傳回字串值，識別命令 (識別碼) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f409-114">Returns a string value identifying the name (ID) of the command.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3f409-115">*原因*</span><span class="sxs-lookup"><span data-stu-id="3f409-115">*Cause*</span></span>       | <span data-ttu-id="3f409-116">傳回值，這個值表示導致說明模式完成的原因。</span><span class="sxs-lookup"><span data-stu-id="3f409-116">Returns a value that indicates what caused the Help mode to complete.</span></span> <span data-ttu-id="3f409-117">1使用者選取了您的應用程式所提供的命令。</span><span class="sxs-lookup"><span data-stu-id="3f409-117">1 The user selected a command supplied by your application.</span></span><br/> <span data-ttu-id="3f409-118">2使用者選取了另一個用戶端的 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="3f409-118">2 The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span><br/> <span data-ttu-id="3f409-119">3使用者已選取 [開啟語音命令] 命令。</span><span class="sxs-lookup"><span data-stu-id="3f409-119">3 The user selected the Open Voice Commands command.</span></span><br/> <span data-ttu-id="3f409-120">4使用者選取了 [關閉語音命令] 命令。</span><span class="sxs-lookup"><span data-stu-id="3f409-120">4 The user selected the Close Voice Commands command.</span></span><br/> <span data-ttu-id="3f409-121">5使用者選取 [顯示 *CharacterName* ] 命令。</span><span class="sxs-lookup"><span data-stu-id="3f409-121">5 The user selected the Show *CharacterName* command.</span></span><br/> <span data-ttu-id="3f409-122">6使用者選取了 [隱藏 *CharacterName* ] 命令。</span><span class="sxs-lookup"><span data-stu-id="3f409-122">6 The user selected the Hide *CharacterName* command.</span></span><br/> <span data-ttu-id="3f409-123">7 (按一下) 字元來選取使用者。</span><span class="sxs-lookup"><span data-stu-id="3f409-123">7 The user selected (clicked) the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="3f409-124">備註</span><span class="sxs-lookup"><span data-stu-id="3f409-124">Remarks</span></span>

<span data-ttu-id="3f409-125">一般而言，當使用者按一下或拖曳字元，或從字元的快顯功能表中選取命令時，[說明] 模式就會完成。</span><span class="sxs-lookup"><span data-stu-id="3f409-125">Typically, Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="3f409-126">按一下其他字元或螢幕上的其他位置，並不會取消說明模式。</span><span class="sxs-lookup"><span data-stu-id="3f409-126">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="3f409-127">設定字元之說明模式的用戶端可以將 [**HelpModeOn**](helpmodeon-property.md) 設定為 **False**，以取消說明模式。</span><span class="sxs-lookup"><span data-stu-id="3f409-127">The client that set Help mode for the character can cancel Help mode by setting [**HelpModeOn**](helpmodeon-property.md) to **False**.</span></span> <span data-ttu-id="3f409-128"> (這不會觸發 **HelpComplete** 事件。 ) </span><span class="sxs-lookup"><span data-stu-id="3f409-128">(This does not trigger the **HelpComplete** event.)</span></span>

<span data-ttu-id="3f409-129">當使用者從 [說明] 模式中的字元快顯功能表選取命令時，伺服器會移除功能表、使用 [**命令指定的**](helpcontextid-property.md)協助工具來呼叫說明，並傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="3f409-129">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="3f409-130">與內容相關的 (也稱為「這是什麼？ ) 說明視窗會顯示在指標位置。</span><span class="sxs-lookup"><span data-stu-id="3f409-130">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="3f409-131">如果使用者選取語音輸入的命令，則會在字元上顯示 [說明] 視窗。</span><span class="sxs-lookup"><span data-stu-id="3f409-131">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="3f409-132">如果字元是在螢幕上，視窗會在畫面上顯示最接近字元的目前位置。</span><span class="sxs-lookup"><span data-stu-id="3f409-132">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="3f409-133">如果伺服器將名稱以空字串的形式傳回 ( "" ) ，表示使用者已選取伺服器提供的命令。</span><span class="sxs-lookup"><span data-stu-id="3f409-133">If the server returns Name as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="3f409-134">此事件只會傳送至用戶端應用程式，該應用程式會將字元放在說明模式中。</span><span class="sxs-lookup"><span data-stu-id="3f409-134">This event is sent only to the client application that places the character in Help mode.</span></span>

### <a name="see-also"></a><span data-ttu-id="3f409-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f409-135">See Also</span></span>

<span data-ttu-id="3f409-136">[**HelpModeOn 屬性**](helpmodeon-property.md)， [**屬性內容屬性**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="3f409-136">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

