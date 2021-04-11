---
title: 'MM_JOY2MOVE 訊息 (Mmsystem .h) '
description: MM \_ JOY2MOVE 訊息會通知視窗，該視窗已捕捉到搖桿的位置已變更。
ms.assetid: 8dc1c092-3947-43d5-8504-a4e4e121fbcb
keywords:
- MM_JOY2MOVE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY2MOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8921f0ae76d05c429d6750944a26662c1276af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093984"
---
# <a name="mm_joy2move-message"></a><span data-ttu-id="0d2ef-104">MM \_ JOY2MOVE 訊息</span><span class="sxs-lookup"><span data-stu-id="0d2ef-104">MM\_JOY2MOVE message</span></span>

<span data-ttu-id="0d2ef-105">**MM \_ JOY2MOVE** 訊息會通知視窗，該視窗已捕捉到搖桿的位置已變更。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-105">The **MM\_JOY2MOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position has changed.</span></span>


```C++
MM_JOY2MOVE 
fwButtons = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="0d2ef-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d2ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d2ef-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="0d2ef-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="0d2ef-108">識別按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="0d2ef-109">它可以是下列其中一個或多個值：</span><span class="sxs-lookup"><span data-stu-id="0d2ef-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="0d2ef-110">需求</span><span class="sxs-lookup"><span data-stu-id="0d2ef-110">Requirement</span></span> | <span data-ttu-id="0d2ef-111">值</span><span class="sxs-lookup"><span data-stu-id="0d2ef-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="0d2ef-112">歡樂 \_ BUTTON1</span><span class="sxs-lookup"><span data-stu-id="0d2ef-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="0d2ef-113">第一個搖桿按鈕已按下。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="0d2ef-114">歡樂 \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="0d2ef-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="0d2ef-115">按下第二個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="0d2ef-116">歡樂 \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="0d2ef-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="0d2ef-117">按下第三個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="0d2ef-118">歡樂 \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="0d2ef-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="0d2ef-119">按第四個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="0d2ef-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span><span class="sxs-lookup"><span data-stu-id="0d2ef-120"><span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*</span></span>
</dt> <dd>

<span data-ttu-id="0d2ef-121">搖桿相對於工作區左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-121">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="0d2ef-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span><span class="sxs-lookup"><span data-stu-id="0d2ef-122"><span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*</span></span>
</dt> <dd>

<span data-ttu-id="0d2ef-123">操縱杆的 y 座標，相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="0d2ef-123">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d2ef-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d2ef-124">Requirements</span></span>



| <span data-ttu-id="0d2ef-125">需求</span><span class="sxs-lookup"><span data-stu-id="0d2ef-125">Requirement</span></span> | <span data-ttu-id="0d2ef-126">值</span><span class="sxs-lookup"><span data-stu-id="0d2ef-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d2ef-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d2ef-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0d2ef-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d2ef-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0d2ef-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d2ef-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0d2ef-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0d2ef-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0d2ef-131">標頭</span><span class="sxs-lookup"><span data-stu-id="0d2ef-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d2ef-132"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="0d2ef-132"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d2ef-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d2ef-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2ef-134">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="0d2ef-134">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="0d2ef-135">多媒體操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="0d2ef-135">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





