---
title: DragComplete 事件
description: DragComplete 事件
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a02fe98e4cf3cdefc1b7734305067550e4923
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969463"
---
# <a name="dragcomplete-event"></a><span data-ttu-id="27312-103">DragComplete 事件</span><span class="sxs-lookup"><span data-stu-id="27312-103">DragComplete Event</span></span>

<span data-ttu-id="27312-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="27312-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="27312-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="27312-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="27312-106">發生于使用者完成拖曳字元時。</span><span class="sxs-lookup"><span data-stu-id="27312-106">Occurs when the user completes dragging a character.</span></span>

</dd> <dt>

<span data-ttu-id="27312-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="27312-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="27312-108">**子\*\*\*代理程式 \* \* \* \_ DragComplete* \*  **(ByVal** *CharacterID*， **byval** *按鈕*， **byval** *Shift*， **byval** *X*， **byval** *Y \* \* \* )**</span><span class="sxs-lookup"><span data-stu-id="27312-108">**Sub** *agent\*\*\*\_DragComplete*\* **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *Shift*, **ByVal** *X*, **ByVal** *Y\*\*\*)*\*</span></span>



| <span data-ttu-id="27312-109">部分</span><span class="sxs-lookup"><span data-stu-id="27312-109">Part</span></span>          | <span data-ttu-id="27312-110">描述</span><span class="sxs-lookup"><span data-stu-id="27312-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27312-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="27312-111">*CharacterID*</span></span> | <span data-ttu-id="27312-112">以字串形式傳回拖曳字元的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27312-112">Returns the ID of the dragged character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="27312-113">*按鈕*</span><span class="sxs-lookup"><span data-stu-id="27312-113">*Button*</span></span>      | <span data-ttu-id="27312-114">傳回整數，這個整數會識別已按下並釋放以引發事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="27312-114">Returns an integer that identifies the button that was pressed and released to cause the event.</span></span> <span data-ttu-id="27312-115">按鈕引數是位在左按鈕 (位 0) 、右按鈕 (位 1) ，以及中間按鈕 (位 2) 的位位。</span><span class="sxs-lookup"><span data-stu-id="27312-115">The button argument is a bitfield with bits corresponding to the left button (bit 0), right button (bit 1), and middle button (bit 2).</span></span> <span data-ttu-id="27312-116">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="27312-116">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="27312-117">只會設定其中一個位，表示造成事件的按鈕。</span><span class="sxs-lookup"><span data-stu-id="27312-117">Only one of the bits is set, indicating the button that caused the event.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="27312-118">*Shift 鍵*</span><span class="sxs-lookup"><span data-stu-id="27312-118">*Shift*</span></span>       | <span data-ttu-id="27312-119">當按下或放開按鈕引數中所指定的按鈕時，傳回對應至 SHIFT、CTRL 和 ALT 鍵狀態的整數。</span><span class="sxs-lookup"><span data-stu-id="27312-119">Returns an integer that corresponds to the state of the SHIFT, CTRL, and ALT keys when the button specified in the button argument is pressed or released.</span></span> <span data-ttu-id="27312-120">如果金鑰已關閉，則會設定位。</span><span class="sxs-lookup"><span data-stu-id="27312-120">A bit is set if the key is down.</span></span> <span data-ttu-id="27312-121">Shift 引數是具有最高有效位（對應至 SHIFT 鍵 (bit 0) 、CTRL 鍵 (bit 1) 和 ALT 鍵 (bit 2) 的位位。</span><span class="sxs-lookup"><span data-stu-id="27312-121">The shift argument is a bitfield with the least-significant bits corresponding to the SHIFT key (bit 0), the CTRL key (bit 1), and the ALT key (bit 2).</span></span> <span data-ttu-id="27312-122">這些位會分別對應至值1、2和4。</span><span class="sxs-lookup"><span data-stu-id="27312-122">These bits correspond to the values 1, 2, and 4, respectively.</span></span> <span data-ttu-id="27312-123">Shift 引數表示這些索引鍵的狀態。</span><span class="sxs-lookup"><span data-stu-id="27312-123">The shift argument indicates the state of these keys.</span></span> <span data-ttu-id="27312-124">您可以設定部分、全部或全部的位，表示未按下部分、全部或未按下任何鍵。</span><span class="sxs-lookup"><span data-stu-id="27312-124">Some, all, or none of the bits can be set, indicating that some, all, or none of the keys are pressed.</span></span> <span data-ttu-id="27312-125">例如，如果按下 CTRL 和 ALT，shift 的值會是6。</span><span class="sxs-lookup"><span data-stu-id="27312-125">For example, if both CTRL and ALT were pressed, the value of shift would be 6.</span></span> |
| <span data-ttu-id="27312-126">*X、Y*</span><span class="sxs-lookup"><span data-stu-id="27312-126">*X,Y*</span></span>         | <span data-ttu-id="27312-127">傳回整數，這個整數會指定滑鼠指標的目前位置。</span><span class="sxs-lookup"><span data-stu-id="27312-127">Returns an integer that specifies the current location of the mouse pointer.</span></span> <span data-ttu-id="27312-128">X 和 Y 值一律以圖元表示，相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="27312-128">The X and Y values are always expressed in pixels, relative to the upper left corner of the screen.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="27312-129">備註</span><span class="sxs-lookup"><span data-stu-id="27312-129">Remarks</span></span>

<span data-ttu-id="27312-130">此事件只會傳送到字元的輸入-主動用戶端。</span><span class="sxs-lookup"><span data-stu-id="27312-130">This event is sent only to the input-active client of a character.</span></span> <span data-ttu-id="27312-131">當使用者拖曳沒有輸入-主動用戶端的字元時，伺服器會將它的最後一個輸入-主動用戶端設定為目前的輸入-主動用戶端，將 [**ActivateInput**](activateinput-event.md) 事件傳送到該用戶端，然後傳送 [**DragStart**](dragstart-event.md) 和 **DragComplete** 事件。</span><span class="sxs-lookup"><span data-stu-id="27312-131">When the user drags a character with no input-active client, the server sets its last input-active client as the current input-active client, sending the [**ActivateInput**](activateinput-event.md) event to that client, and then sending the [**DragStart**](dragstart-event.md) and **DragComplete** events.</span></span>

### <a name="see-also"></a><span data-ttu-id="27312-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27312-132">See Also</span></span>

[<span data-ttu-id="27312-133">**DragStart 事件**</span><span class="sxs-lookup"><span data-stu-id="27312-133">**DragStart event**</span></span>](dragstart-event.md)


 

 




