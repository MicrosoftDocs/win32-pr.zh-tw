---
title: 點選事件
description: 點選事件
ms.assetid: 772029d5-97b6-49d8-a989-04f0fc429aca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3956d19e833a3e0a5f71192b2846ef9cb270ad10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372461"
---
# <a name="click-event"></a><span data-ttu-id="177bc-103">點選事件</span><span class="sxs-lookup"><span data-stu-id="177bc-103">Click Event</span></span>

<span data-ttu-id="177bc-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="177bc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="177bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="177bc-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="177bc-106">當使用者按一下字元或字元的圖示時發生。</span><span class="sxs-lookup"><span data-stu-id="177bc-106">Occurs when the user clicks a character or the character's icon.</span></span>

</dd> <dt>

<span data-ttu-id="177bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="177bc-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="177bc-108">**子\*\*\*代理程式 \* \* \* \_ 按一下* \*  **(byval** *CharacterID*， **byval** *按鈕*， **byval** *Shift*， **byval** *X*， **byval** *Y \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="177bc-108">**Sub** *agent\*\*\*\_Click*\* **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="177bc-109">部分</span><span class="sxs-lookup"><span data-stu-id="177bc-109">Part</span></span>          | <span data-ttu-id="177bc-110">描述</span><span class="sxs-lookup"><span data-stu-id="177bc-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="177bc-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="177bc-111">*CharacterID*</span></span> | <span data-ttu-id="177bc-112">以字串形式傳回已按下字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="177bc-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="177bc-113">*按鈕*</span><span class="sxs-lookup"><span data-stu-id="177bc-113">*Button*</span></span>      | <span data-ttu-id="177bc-114">傳回整數，這個整數會識別已按下並釋放以引發事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="177bc-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="177bc-115">按鈕引數是位在左按鈕 (位 0) 、右按鈕 (位 1) ，以及中間按鈕 (位 2) 的位位。</span><span class="sxs-lookup"><span data-stu-id="177bc-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="177bc-116">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="177bc-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="177bc-117">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="177bc-117">Only one of the bits is set, indicating the button that caused the event.</span></span> <span data-ttu-id="177bc-118">如果字元包含工作列圖示，而且也設定了位13，則會在工作列圖示上按一下。</span><span class="sxs-lookup"><span data-stu-id="177bc-118">If the character includes a taskbar icon, and bit 13 is also set, the click occurred on the taskbar icon.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="177bc-119">*Shift 鍵*</span><span class="sxs-lookup"><span data-stu-id="177bc-119">*Shift*</span></span>       | <span data-ttu-id="177bc-120">當按下或放開按鈕引數中所指定的按鈕時，傳回對應至 SHIFT、CTRL 和 ALT 鍵狀態的整數。</span><span class="sxs-lookup"><span data-stu-id="177bc-120">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="177bc-121">如果金鑰已關閉，則會設定位。</span><span class="sxs-lookup"><span data-stu-id="177bc-121">A bit is set if the key is down.</span></span> <span data-ttu-id="177bc-122">Shift 引數是具有最高有效位（對應至 SHIFT 鍵 (bit 0) 、CTRL 鍵 (bit 1) 和 ALT 鍵 (bit 2) 的位位。</span><span class="sxs-lookup"><span data-stu-id="177bc-122">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="177bc-123">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="177bc-123">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="177bc-124">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="177bc-124">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="177bc-125">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="177bc-125">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="177bc-126">例如，如果按下 CTRL 和 ALT，shift 的值會是6。</span><span class="sxs-lookup"><span data-stu-id="177bc-126">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="177bc-127">*X、Y*</span><span class="sxs-lookup"><span data-stu-id="177bc-127">*X,Y*</span></span>         | <span data-ttu-id="177bc-128">傳回整數，這個整數會指定滑鼠指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="177bc-128">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="177bc-129">X 和 Y 值一律以圖元表示，相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="177bc-129">The X and Y values are always expressed in pixels, relative to the upper-left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="177bc-130">備註</span><span class="sxs-lookup"><span data-stu-id="177bc-130">Remarks</span></span>

<span data-ttu-id="177bc-131">此事件只會傳送到字元的輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="177bc-131">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="177bc-132">當使用者按一下沒有輸入-主動用戶端的字元或其工作列圖示時，伺服器會將事件傳送到其作用中用戶端。</span><span class="sxs-lookup"><span data-stu-id="177bc-132">When the user clicks a character or its taskbar icon with no input-active client, the server sends the event to its active client.</span></span> <span data-ttu-id="177bc-133">如果顯示的字元 ([**可見**](visible-property.md)的  =  **True**) ，使用者的動作也會將字元的最後輸入-使用中用戶端設定為目前輸入-主動用戶端，將 [**ActivateInput**](activateinput-event.md)事件傳送到該用戶端，然後再傳送 **Click** 事件。</span><span class="sxs-lookup"><span data-stu-id="177bc-133">If the character is visible ([**Visible**](visible-property.md) = **True**), the user's action also sets the character's last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the **Click** event.</span></span> <span data-ttu-id="177bc-134">如果隱藏字元 (可見的  =  **False**) ，而且使用者按一下使用按鈕1的字元工作列圖示，則也會自動顯示該字元。</span><span class="sxs-lookup"><span data-stu-id="177bc-134">If the character is hidden (**Visible** = **False**), and the user clicks the character's taskbar icon using button 1, the character is also automatically shown.</span></span>

> [!Note]  
> <span data-ttu-id="177bc-135">按一下字元並不會停用所有其他字元輸出 (所有字元) 。</span><span class="sxs-lookup"><span data-stu-id="177bc-135">Clicking a character does not disable all other character output (all characters).</span></span> <span data-ttu-id="177bc-136">不過，按接聽鍵會排清輸入-主動字元的輸出，並觸發 [**RequestComplete**](requestcomplete-event.md) 事件，並傳遞 [要求。](status-property.md) 表示用戶端佇列已中斷的狀態。</span><span class="sxs-lookup"><span data-stu-id="177bc-136">However, pressing the Listening key does flush the input-active character's output and triggers the [**RequestComplete**](requestcomplete-event.md) event, passing a [Request.Status](status-property.md) that indicates that the client's queue was interrupted.</span></span>

 

 

 




