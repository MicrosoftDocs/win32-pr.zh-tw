---
title: 'MM_JOY2BUTTONUP 訊息 (Mmsystem .h) '
description: MM \_ JOY2BUTTONUP 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID2 已釋放按鈕。
ms.assetid: da024466-7cd3-42ec-90a7-1468eb42841e
keywords:
- MM_JOY2BUTTONUP message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY2BUTTONUP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7a4f2d23739fc72a6898e2b53fc3e1c330687f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966157"
---
# <a name="mm_joy2buttonup-message"></a><span data-ttu-id="86576-104">MM \_ JOY2BUTTONUP 訊息</span><span class="sxs-lookup"><span data-stu-id="86576-104">MM\_JOY2BUTTONUP message</span></span>

<span data-ttu-id="86576-105">**MM \_ JOY2BUTTONUP** 訊息會通知已捕捉到搖桿的視窗 JOYSTICKID2 已釋放按鈕。</span><span class="sxs-lookup"><span data-stu-id="86576-105">The **MM\_JOY2BUTTONUP** message notifies the window that has captured joystick JOYSTICKID2 that a button has been released.</span></span>


```C++
MM_JOY2BUTTONUP 
fwButton = wParam; 
xPos = LOWORD(lParam); 
yPos = HIWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="86576-106">參數</span><span class="sxs-lookup"><span data-stu-id="86576-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86576-107">**fwButtons**</span><span class="sxs-lookup"><span data-stu-id="86576-107">**fwButtons**</span></span> 
</dt> <dd>

<span data-ttu-id="86576-108">識別已變更狀態的按鈕和已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="86576-108">Identifies the button that has changed state and the buttons that are pressed.</span></span> <span data-ttu-id="86576-109">可以是下列其中一項：</span><span class="sxs-lookup"><span data-stu-id="86576-109">It can be one of the following:</span></span>



| <span data-ttu-id="86576-110">值</span><span class="sxs-lookup"><span data-stu-id="86576-110">Value</span></span>                                                                                                                                                            | <span data-ttu-id="86576-111">意義</span><span class="sxs-lookup"><span data-stu-id="86576-111">Meaning</span></span>                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="JOY_BUTTON1CHG"></span><span id="joy_button1chg"></span><dl> <span data-ttu-id="86576-112"><dt>**歡樂 \_ BUTTON1CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-112"><dt>**JOY\_BUTTON1CHG**</dt></span></span> </dl> | <span data-ttu-id="86576-113">第一個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="86576-113">First joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON2CHG"></span><span id="joy_button2chg"></span><dl> <span data-ttu-id="86576-114"><dt>**歡樂 \_ BUTTON2CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-114"><dt>**JOY\_BUTTON2CHG**</dt></span></span> </dl> | <span data-ttu-id="86576-115">第二個操縱杆按鈕已變更狀態。</span><span class="sxs-lookup"><span data-stu-id="86576-115">Second joystick button has changed state.</span></span><br/> |
| <span id="JOY_BUTTON3CHG"></span><span id="joy_button3chg"></span><dl> <span data-ttu-id="86576-116"><dt>**歡樂 \_ BUTTON3CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-116"><dt>**JOY\_BUTTON3CHG**</dt></span></span> </dl> | <span data-ttu-id="86576-117">第三個搖桿按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="86576-117">Third joystick button has changed state.</span></span><br/>  |
| <span id="JOY_BUTTON4CHG"></span><span id="joy_button4chg"></span><dl> <span data-ttu-id="86576-118"><dt>**歡樂 \_ BUTTON4CHG**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-118"><dt>**JOY\_BUTTON4CHG**</dt></span></span> </dl> | <span data-ttu-id="86576-119">第四個操縱杆按鈕的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="86576-119">Fourth joystick button has changed state.</span></span><br/> |



 

<span data-ttu-id="86576-120">以及下列一或多項：</span><span class="sxs-lookup"><span data-stu-id="86576-120">and one or more of the following:</span></span>



| <span data-ttu-id="86576-121">值</span><span class="sxs-lookup"><span data-stu-id="86576-121">Value</span></span>                                                                                                                                                   | <span data-ttu-id="86576-122">意義</span><span class="sxs-lookup"><span data-stu-id="86576-122">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="JOY_BUTTON1"></span><span id="joy_button1"></span><dl> <span data-ttu-id="86576-123"><dt>**歡樂 \_ BUTTON1**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-123"><dt>**JOY\_BUTTON1**</dt></span></span> </dl> | <span data-ttu-id="86576-124">第一個搖桿按鈕已按下。</span><span class="sxs-lookup"><span data-stu-id="86576-124">First joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON2"></span><span id="joy_button2"></span><dl> <span data-ttu-id="86576-125"><dt>**歡樂 \_ BUTTON2**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-125"><dt>**JOY\_BUTTON2**</dt></span></span> </dl> | <span data-ttu-id="86576-126">按下第二個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="86576-126">Second joystick button is pressed.</span></span><br/> |
| <span id="JOY_BUTTON3"></span><span id="joy_button3"></span><dl> <span data-ttu-id="86576-127"><dt>**歡樂 \_ BUTTON3**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-127"><dt>**JOY\_BUTTON3**</dt></span></span> </dl> | <span data-ttu-id="86576-128">按下第三個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="86576-128">Third joystick button is pressed.</span></span><br/>  |
| <span id="JOY_BUTTON4"></span><span id="joy_button4"></span><dl> <span data-ttu-id="86576-129"><dt>**歡樂 \_ BUTTON4**</dt></span><span class="sxs-lookup"><span data-stu-id="86576-129"><dt>**JOY\_BUTTON4**</dt></span></span> </dl> | <span data-ttu-id="86576-130">按第四個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="86576-130">Fourth joystick button is pressed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="86576-131">**xPos**</span><span class="sxs-lookup"><span data-stu-id="86576-131">**xPos**</span></span> 
</dt> <dd>

<span data-ttu-id="86576-132">搖桿相對於工作區左上角的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="86576-132">The x-coordinates of the joystick relative to the upper left corner of the client area.</span></span>

</dd> <dt>

<span data-ttu-id="86576-133">**yPos**</span><span class="sxs-lookup"><span data-stu-id="86576-133">**yPos**</span></span> 
</dt> <dd>

<span data-ttu-id="86576-134">操縱杆的 y 座標，相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="86576-134">The y-coordinate of the joystick relative to the upper left corner of the client area.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="86576-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="86576-135">Requirements</span></span>



| <span data-ttu-id="86576-136">需求</span><span class="sxs-lookup"><span data-stu-id="86576-136">Requirement</span></span> | <span data-ttu-id="86576-137">值</span><span class="sxs-lookup"><span data-stu-id="86576-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86576-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86576-138">Minimum supported client</span></span><br/> | <span data-ttu-id="86576-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86576-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="86576-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86576-140">Minimum supported server</span></span><br/> | <span data-ttu-id="86576-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86576-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="86576-142">標頭</span><span class="sxs-lookup"><span data-stu-id="86576-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="86576-143"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="86576-143"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86576-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86576-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86576-145">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="86576-145">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="86576-146">多媒體操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="86576-146">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





