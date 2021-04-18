---
title: 'MM_JOY1BUTTONDOWN 訊息 (Mmsystem .h) '
description: MM \_ JOY1BUTTONDOWN 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID1 已按下按鈕。
ms.assetid: 764f4bb4-134d-46b8-badb-3fb06af31e13
keywords:
- MM_JOY1BUTTONDOWN message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONDOWN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cefb70e5dd47fc14b39dcdeb59043b6827e7b89b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464500"
---
# <a name="mm_joy1buttondown-message"></a><span data-ttu-id="6701a-104">MM \_ JOY1BUTTONDOWN 訊息</span><span class="sxs-lookup"><span data-stu-id="6701a-104">MM\_JOY1BUTTONDOWN message</span></span>

<span data-ttu-id="6701a-105">**MM \_ JOY1BUTTONDOWN** 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID1 已按下按鈕。</span><span class="sxs-lookup"><span data-stu-id="6701a-105">The **MM\_JOY1BUTTONDOWN** message notifies the window that has captured joystick JOYSTICKID1 that a button has been pressed.</span></span>


```C++
MM_JOY1BUTTONDOWN 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="6701a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6701a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6701a-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="6701a-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="6701a-108">識別已變更狀態的按鈕和已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="6701a-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="6701a-109">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="6701a-109">It can be one of the following:</span></span>



| <span data-ttu-id="6701a-110">需求</span><span class="sxs-lookup"><span data-stu-id="6701a-110">Requirement</span></span> | <span data-ttu-id="6701a-111">值</span><span class="sxs-lookup"><span data-stu-id="6701a-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="6701a-112">歡樂 \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="6701a-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="6701a-113">第一個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="6701a-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="6701a-114">歡樂 \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="6701a-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="6701a-115">第二個操縱杆按鈕已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="6701a-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="6701a-116">歡樂 \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="6701a-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="6701a-117">第三個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="6701a-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="6701a-118">歡樂 \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="6701a-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="6701a-119">第四個操縱杆按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="6701a-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="6701a-120">以及下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="6701a-120">and one or more of the following:</span></span>



| <span data-ttu-id="6701a-121">需求</span><span class="sxs-lookup"><span data-stu-id="6701a-121">Requirement</span></span> | <span data-ttu-id="6701a-122">值</span><span class="sxs-lookup"><span data-stu-id="6701a-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="6701a-123">歡樂 \_ BUTTON1</span><span class="sxs-lookup"><span data-stu-id="6701a-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="6701a-124">第一個搖桿按鈕已按下。</span><span class="sxs-lookup"><span data-stu-id="6701a-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="6701a-125">歡樂 \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="6701a-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="6701a-126">按下第二個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="6701a-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="6701a-127">歡樂 \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="6701a-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="6701a-128">按下第三個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="6701a-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="6701a-129">歡樂 \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="6701a-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="6701a-130">按第四個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="6701a-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6701a-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="6701a-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="6701a-132">搖桿相對於工作區左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="6701a-132">The x-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="6701a-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="6701a-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="6701a-134">操縱杆的 y 座標，相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="6701a-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6701a-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="6701a-135">Requirements</span></span>



| <span data-ttu-id="6701a-136">需求</span><span class="sxs-lookup"><span data-stu-id="6701a-136">Requirement</span></span> | <span data-ttu-id="6701a-137">值</span><span class="sxs-lookup"><span data-stu-id="6701a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6701a-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6701a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6701a-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6701a-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6701a-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6701a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6701a-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6701a-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6701a-142">標頭</span><span class="sxs-lookup"><span data-stu-id="6701a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6701a-143"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6701a-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6701a-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6701a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6701a-145">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="6701a-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="6701a-146">多媒體操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="6701a-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





