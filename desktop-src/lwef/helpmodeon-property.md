---
title: HelpModeOn 屬性
description: HelpModeOn 屬性
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673483"
---
# <a name="helpmodeon-property"></a><span data-ttu-id="68491-103">HelpModeOn 屬性</span><span class="sxs-lookup"><span data-stu-id="68491-103">HelpModeOn Property</span></span>

<span data-ttu-id="68491-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="68491-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="68491-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="68491-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="68491-106">傳回或設定是否為字元的即時線上說明模式。</span><span class="sxs-lookup"><span data-stu-id="68491-106">Returns or sets whether context-sensitive Help mode is on for the character.</span></span>

</dd> <dt>

<span data-ttu-id="68491-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="68491-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="68491-108">*代理程式。\*\*\*字元 (*\*\* 」CharacterID \* \* \* ) 。HelpModeOn\* \*  \[  =  *布林值*\]</span><span class="sxs-lookup"><span data-stu-id="68491-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").HelpModeOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="68491-109">部分</span><span class="sxs-lookup"><span data-stu-id="68491-109">Part</span></span>      | <span data-ttu-id="68491-110">描述</span><span class="sxs-lookup"><span data-stu-id="68491-110">Description</span></span>                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68491-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="68491-111">*boolean*</span></span> | <span data-ttu-id="68491-112">布林運算式，指定是否開啟即時線上說明模式。</span><span class="sxs-lookup"><span data-stu-id="68491-112">A Boolean expression specifying whether context-sensitive Help mode is on.</span></span> <span data-ttu-id="68491-113">**True** 說明模式為開啟。</span><span class="sxs-lookup"><span data-stu-id="68491-113">**True** Help mode is on.</span></span> <br/> <span data-ttu-id="68491-114">**False** (預設) 說明模式為關閉。</span><span class="sxs-lookup"><span data-stu-id="68491-114">**False** (Default) Help mode is off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68491-115">備註</span><span class="sxs-lookup"><span data-stu-id="68491-115">Remarks</span></span>

<span data-ttu-id="68491-116">當您將這個屬性設定為 **True** 時，滑鼠指標會在移至字元上方或移至字元的快顯功能表時，變更為內容相關的說明影像。</span><span class="sxs-lookup"><span data-stu-id="68491-116">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="68491-117">當使用者按一下或拖曳字元，或按一下字元快顯功能表中的專案時，伺服器會觸發 [**HelpComplete**](helpcomplete-event.md) 事件並離開說明模式。</span><span class="sxs-lookup"><span data-stu-id="68491-117">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**HelpComplete**](helpcomplete-event.md) event and exits Help mode.</span></span>

<span data-ttu-id="68491-118">在 [說明] 模式中，除非您將 [**AutoPopupMenu**](autopopupmenu-property.md)屬性設定為 **True**，否則伺服器不會傳送 [**Click**](click-event.md)、 [**DragStart**](dragstart-event.md)、 [**DragComplete**](dragcomplete-event.md)和 [**命令**](command-event.md)事件。</span><span class="sxs-lookup"><span data-stu-id="68491-118">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md), and [**Command**](command-event.md) events, unless you set the [**AutoPopupMenu**](autopopupmenu-property.md) property to **True**.</span></span> <span data-ttu-id="68491-119">在這種情況下，伺服器會傳送 **Click** 事件 (不會離開說明模式) ，而只有滑鼠右鍵可讓您顯示快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="68491-119">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="68491-120">這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。</span><span class="sxs-lookup"><span data-stu-id="68491-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="68491-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68491-121">See Also</span></span>

[<span data-ttu-id="68491-122">**HelpComplete 事件**</span><span class="sxs-lookup"><span data-stu-id="68491-122">**HelpComplete event**</span></span>](helpcomplete-event.md)


 

 





