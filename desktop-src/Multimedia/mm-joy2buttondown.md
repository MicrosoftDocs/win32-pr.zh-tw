---
title: 'MM_JOY2BUTTONDOWN 訊息 (Mmsystem .h) '
description: MM \_ JOY2BUTTONDOWN 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID2 已按下按鈕。
ms.assetid: b4cd48ea-91ad-48e9-b0ae-58d8ee124171
keywords:
- MM_JOY2BUTTONDOWN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f155fcdc21247e01fd5d730f3f7d4daaba705e65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106984951"
---
# <a name="mm_joy2buttondown-message"></a><span data-ttu-id="33368-104">MM \_ JOY2BUTTONDOWN 訊息</span><span class="sxs-lookup"><span data-stu-id="33368-104">MM\_JOY2BUTTONDOWN message</span></span>

<span data-ttu-id="33368-105">**MM \_ JOY2BUTTONDOWN** 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID2 已按下按鈕。</span><span class="sxs-lookup"><span data-stu-id="33368-105">The **MM\_JOY2BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID2 that a button has been pressed.</span></span>


```C++
MM_JOY2BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="33368-106">參數</span><span class="sxs-lookup"><span data-stu-id="33368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33368-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="33368-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="33368-108">識別已變更狀態的按鈕和已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="33368-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="33368-109">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="33368-109">It can be one of the following:</span></span>



| <span data-ttu-id="33368-110">需求</span><span class="sxs-lookup"><span data-stu-id="33368-110">Requirement</span></span> | <span data-ttu-id="33368-111">值</span><span class="sxs-lookup"><span data-stu-id="33368-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="33368-112">歡樂 \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="33368-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="33368-113">第一個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="33368-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="33368-114">歡樂 \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="33368-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="33368-115">第二個操縱杆按鈕已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="33368-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="33368-116">歡樂 \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="33368-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="33368-117">第三個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="33368-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="33368-118">歡樂 \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="33368-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="33368-119">第四個操縱杆按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="33368-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="33368-120">以及下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="33368-120">and one or more of the following:</span></span>



| <span data-ttu-id="33368-121">需求</span><span class="sxs-lookup"><span data-stu-id="33368-121">Requirement</span></span> | <span data-ttu-id="33368-122">值</span><span class="sxs-lookup"><span data-stu-id="33368-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="33368-123">歡樂 \_ BUTTON1</span><span class="sxs-lookup"><span data-stu-id="33368-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="33368-124">第一個搖桿按鈕已按下。</span><span class="sxs-lookup"><span data-stu-id="33368-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="33368-125">歡樂 \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="33368-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="33368-126">按下第二個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="33368-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="33368-127">歡樂 \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="33368-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="33368-128">按下第三個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="33368-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="33368-129">歡樂 \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="33368-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="33368-130">按第四個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="33368-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="33368-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="33368-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="33368-132">搖桿相對於工作區左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="33368-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="33368-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="33368-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="33368-134">操縱杆的 y 座標，相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="33368-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33368-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="33368-135">Requirements</span></span>



| <span data-ttu-id="33368-136">需求</span><span class="sxs-lookup"><span data-stu-id="33368-136">Requirement</span></span> | <span data-ttu-id="33368-137">值</span><span class="sxs-lookup"><span data-stu-id="33368-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33368-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="33368-138">Minimum supported client</span></span><br/> | <span data-ttu-id="33368-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33368-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="33368-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="33368-140">Minimum supported server</span></span><br/> | <span data-ttu-id="33368-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="33368-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="33368-142">標頭</span><span class="sxs-lookup"><span data-stu-id="33368-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="33368-143"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="33368-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33368-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="33368-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33368-145">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="33368-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="33368-146">多媒體操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="33368-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





