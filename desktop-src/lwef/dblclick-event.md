---
title: DblClick 事件
description: DblClick 事件
ms.assetid: 81ed5396-a2dc-49fe-820f-61ca0935fe85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b900b8a8b79345c50749a4355deeb05fdc1220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301419"
---
# <a name="dblclick-event"></a><span data-ttu-id="5c356-103">DblClick 事件</span><span class="sxs-lookup"><span data-stu-id="5c356-103">DblClick Event</span></span>

<span data-ttu-id="5c356-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5c356-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="5c356-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="5c356-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="5c356-106">發生于使用者按兩下字元時。</span><span class="sxs-lookup"><span data-stu-id="5c356-106">Occurs when the user double-clicks a character.</span></span>

</dd> <dt>

<span data-ttu-id="5c356-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="5c356-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="5c356-108">**子\*\*\*代理程式 \* \* \* \_ DblClick* \*  **(ByVal** *CharacterID*， **byval** *按鈕*， **byval** *Shift*， **byval** *X*， **byval** *Y \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="5c356-108">**Sub** *agent\*\*\*\_DblClick*\* **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="5c356-109">部分</span><span class="sxs-lookup"><span data-stu-id="5c356-109">Part</span></span>          | <span data-ttu-id="5c356-110">描述</span><span class="sxs-lookup"><span data-stu-id="5c356-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c356-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="5c356-111">*CharacterID*</span></span> | <span data-ttu-id="5c356-112">以字串形式傳回按兩下字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c356-112">Returns the ID of the double-clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="5c356-113">*按鈕*</span><span class="sxs-lookup"><span data-stu-id="5c356-113">*Button*</span></span>      | <span data-ttu-id="5c356-114">傳回整數，這個整數會識別已按下並釋放以引發事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="5c356-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="5c356-115">按鈕引數是位在左按鈕 (位 0) 、右按鈕 (位 1) ，以及中間按鈕 (位 2) 的位位。</span><span class="sxs-lookup"><span data-stu-id="5c356-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="5c356-116">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="5c356-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="5c356-117">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="5c356-117">Only one of the bits is set, indicating the button that caused the event.</span></span> <span data-ttu-id="5c356-118">如果字元包含工作列圖示，則如果同時設定了 bit 13，則會在工作列圖示上按一下。</span><span class="sxs-lookup"><span data-stu-id="5c356-118">If the character includes a taskbar icon, if bit 13 is also set, the click occurred on the taskbar icon.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="5c356-119">*Shift 鍵*</span><span class="sxs-lookup"><span data-stu-id="5c356-119">*Shift*</span></span>       | <span data-ttu-id="5c356-120">當按下或放開按鈕引數中所指定的按鈕時，傳回對應至 SHIFT、CTRL 和 ALT 鍵狀態的整數。</span><span class="sxs-lookup"><span data-stu-id="5c356-120">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="5c356-121">如果金鑰已關閉，則會設定位。</span><span class="sxs-lookup"><span data-stu-id="5c356-121">A bit is set if the key is down.</span></span> <span data-ttu-id="5c356-122">Shift 引數是具有最高有效位（對應至 SHIFT 鍵 (bit 0) 、CTRL 鍵 (bit 1) 和 ALT 鍵 (bit 2) 的位位。</span><span class="sxs-lookup"><span data-stu-id="5c356-122">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="5c356-123">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="5c356-123">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="5c356-124">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="5c356-124">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="5c356-125">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="5c356-125">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="5c356-126">例如，如果按下 CTRL 和 ALT，shift 的值會是6。</span><span class="sxs-lookup"><span data-stu-id="5c356-126">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="5c356-127">*X、Y*</span><span class="sxs-lookup"><span data-stu-id="5c356-127">*X,Y*</span></span>         | <span data-ttu-id="5c356-128">傳回整數，這個整數會指定滑鼠指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="5c356-128">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="5c356-129">X 和 Y 值一律以圖元表示，相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="5c356-129">The X and Y values are always expressed in pixels, relative to the upper-left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="5c356-130">備註</span><span class="sxs-lookup"><span data-stu-id="5c356-130">Remarks</span></span>

<span data-ttu-id="5c356-131">此事件只會傳送到字元的輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="5c356-131">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="5c356-132">當使用者按兩下沒有輸入-主動用戶端的字元或其工作列圖示時，伺服器會將事件傳送至其最後一個輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="5c356-132">When the user double-clicks a character or its taskbar icon with no input-active client, the server sends the event to its last input-active client.</span></span> <span data-ttu-id="5c356-133">如果顯示的字元 ([可見](visible-property.md)的  =  **True**) ，則它也會將使用中用戶端設定為目前輸入-主動用戶端，將 [**ActivateInput**](activateinput-event.md)事件傳送到該用戶端，然後傳送 **DblClick** 事件。</span><span class="sxs-lookup"><span data-stu-id="5c356-133">If the character is visible ([Visible](visible-property.md) = **True**), then it also sets the active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the **DblClick** event.</span></span> <span data-ttu-id="5c356-134">如果隱藏字元 (Visible = **False**) 而使用者使用按鈕1按兩下字元的工作列圖示，它也會自動顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="5c356-134">If the character is hidden (Visible = **False**) and the user double-clicks the character's taskbar icon using button 1, it also automatically shows the character.</span></span>

 

 




