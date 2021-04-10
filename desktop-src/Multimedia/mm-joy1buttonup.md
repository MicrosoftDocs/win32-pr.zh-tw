---
title: 'MM_JOY1BUTTONUP 訊息 (Mmsystem .h) '
description: MM \_ JOY1BUTTONUP 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID1 已釋放按鈕。
ms.assetid: 37f0f87a-4805-4cec-9c0c-9d6b36a3ff0d
keywords:
- MM_JOY1BUTTONUP message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY1BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 007a5d954b9b879f87c5e8ffe2d0774d0d1d85a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106524"
---
# <a name="mm_joy1buttonup-message"></a><span data-ttu-id="d4f71-104">MM \_ JOY1BUTTONUP 訊息</span><span class="sxs-lookup"><span data-stu-id="d4f71-104">MM\_JOY1BUTTONUP message</span></span>

<span data-ttu-id="d4f71-105">**MM \_ JOY1BUTTONUP** 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID1 已釋放按鈕。</span><span class="sxs-lookup"><span data-stu-id="d4f71-105">The **MM\_JOY1BUTTONUP** message notifies the window that has captured joystick JOYSTICKID1 that a button has been released.</span></span>


```C++
MM_JOY1BUTTONUP 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="d4f71-106">參數</span><span class="sxs-lookup"><span data-stu-id="d4f71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4f71-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="d4f71-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="d4f71-108">識別已變更狀態的按鈕和已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="d4f71-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="d4f71-109">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="d4f71-109">It can be one of the following:</span></span>



| <span data-ttu-id="d4f71-110">需求</span><span class="sxs-lookup"><span data-stu-id="d4f71-110">Requirement</span></span> | <span data-ttu-id="d4f71-111">值</span><span class="sxs-lookup"><span data-stu-id="d4f71-111">Value</span></span> |
|-----------------|-------------------------------------------|
| <span data-ttu-id="d4f71-112">歡樂 \_ BUTTON1CHG</span><span class="sxs-lookup"><span data-stu-id="d4f71-112">JOY\_BUTTON1CHG</span></span> | <span data-ttu-id="d4f71-113">第一個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="d4f71-113">First joystick button has changed state.</span></span>  |
| <span data-ttu-id="d4f71-114">歡樂 \_ BUTTON2CHG</span><span class="sxs-lookup"><span data-stu-id="d4f71-114">JOY\_BUTTON2CHG</span></span> | <span data-ttu-id="d4f71-115">第二個操縱杆按鈕已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="d4f71-115">Second joystick button has changed state.</span></span> |
| <span data-ttu-id="d4f71-116">歡樂 \_ BUTTON3CHG</span><span class="sxs-lookup"><span data-stu-id="d4f71-116">JOY\_BUTTON3CHG</span></span> | <span data-ttu-id="d4f71-117">第三個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="d4f71-117">Third joystick button has changed state.</span></span>  |
| <span data-ttu-id="d4f71-118">歡樂 \_ BUTTON4CHG</span><span class="sxs-lookup"><span data-stu-id="d4f71-118">JOY\_BUTTON4CHG</span></span> | <span data-ttu-id="d4f71-119">第四個操縱杆按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="d4f71-119">Fourth joystick button has changed state.</span></span> |



 

<span data-ttu-id="d4f71-120">以及下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="d4f71-120">and one or more of the following:</span></span>



| <span data-ttu-id="d4f71-121">需求</span><span class="sxs-lookup"><span data-stu-id="d4f71-121">Requirement</span></span> | <span data-ttu-id="d4f71-122">值</span><span class="sxs-lookup"><span data-stu-id="d4f71-122">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="d4f71-123">歡樂 \_ BUTTON1</span><span class="sxs-lookup"><span data-stu-id="d4f71-123">JOY\_BUTTON1</span></span> | <span data-ttu-id="d4f71-124">第一個搖桿按鈕已按下。</span><span class="sxs-lookup"><span data-stu-id="d4f71-124">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="d4f71-125">歡樂 \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="d4f71-125">JOY\_BUTTON2</span></span> | <span data-ttu-id="d4f71-126">按下第二個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="d4f71-126">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="d4f71-127">歡樂 \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="d4f71-127">JOY\_BUTTON3</span></span> | <span data-ttu-id="d4f71-128">按下第三個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="d4f71-128">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="d4f71-129">歡樂 \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="d4f71-129">JOY\_BUTTON4</span></span> | <span data-ttu-id="d4f71-130">按第四個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="d4f71-130">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="d4f71-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="d4f71-131"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="d4f71-132">搖桿相對於工作區左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="d4f71-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="d4f71-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="d4f71-133"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="d4f71-134">操縱杆的 y 座標，相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="d4f71-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4f71-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4f71-135">Requirements</span></span>



| <span data-ttu-id="d4f71-136">需求</span><span class="sxs-lookup"><span data-stu-id="d4f71-136">Requirement</span></span> | <span data-ttu-id="d4f71-137">值</span><span class="sxs-lookup"><span data-stu-id="d4f71-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f71-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4f71-138">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f71-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4f71-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d4f71-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4f71-140">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f71-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d4f71-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d4f71-142">標頭</span><span class="sxs-lookup"><span data-stu-id="d4f71-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f71-143"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d4f71-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4f71-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4f71-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f71-145">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="d4f71-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="d4f71-146">多媒體操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="d4f71-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





