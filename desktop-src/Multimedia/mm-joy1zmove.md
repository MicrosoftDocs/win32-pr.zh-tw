---
title: 'MM_JOY1ZMOVE 訊息 (Mmsystem .h) '
description: MM \_ JOY1ZMOVE 訊息會通知視窗，該視窗已捕捉至 Z 軸上的搖桿位置已變更的搖桿 JOYSTICKID1。
ms.assetid: 25d98963-03e6-4276-a132-256e8bbfa73b
keywords:
- MM_JOY1ZMOVE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY1ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d4db3db8c1817f0502ce14cc5328ad666b32c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467085"
---
# <a name="mm_joy1zmove-message"></a><span data-ttu-id="48d87-104">MM \_ JOY1ZMOVE 訊息</span><span class="sxs-lookup"><span data-stu-id="48d87-104">MM\_JOY1ZMOVE message</span></span>

<span data-ttu-id="48d87-105">**MM \_ JOY1ZMOVE** 訊息會通知視窗，該視窗已捕捉至 Z 軸上的搖桿位置已變更的搖桿 JOYSTICKID1。</span><span class="sxs-lookup"><span data-stu-id="48d87-105">The **MM\_JOY1ZMOVE** message notifies the window that has captured joystick JOYSTICKID1 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY1ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="48d87-106">參數</span><span class="sxs-lookup"><span data-stu-id="48d87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48d87-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="48d87-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="48d87-108">識別按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="48d87-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="48d87-109">它可以是下列其中一個或多個值：</span><span class="sxs-lookup"><span data-stu-id="48d87-109">It can be one or more of the following values:</span></span>



| <span data-ttu-id="48d87-110">需求</span><span class="sxs-lookup"><span data-stu-id="48d87-110">Requirement</span></span> | <span data-ttu-id="48d87-111">值</span><span class="sxs-lookup"><span data-stu-id="48d87-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="48d87-112">歡樂 \_ BUTTON1</span><span class="sxs-lookup"><span data-stu-id="48d87-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="48d87-113">第一個搖桿按鈕已按下。</span><span class="sxs-lookup"><span data-stu-id="48d87-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="48d87-114">歡樂 \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="48d87-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="48d87-115">按下第二個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="48d87-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="48d87-116">歡樂 \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="48d87-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="48d87-117">按下第三個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="48d87-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="48d87-118">歡樂 \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="48d87-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="48d87-119">按第四個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="48d87-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="48d87-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span><span class="sxs-lookup"><span data-stu-id="48d87-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="48d87-121">搖桿的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="48d87-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48d87-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="48d87-122">Requirements</span></span>



| <span data-ttu-id="48d87-123">需求</span><span class="sxs-lookup"><span data-stu-id="48d87-123">Requirement</span></span> | <span data-ttu-id="48d87-124">值</span><span class="sxs-lookup"><span data-stu-id="48d87-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d87-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48d87-125">Minimum supported client</span></span><br/> | <span data-ttu-id="48d87-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48d87-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="48d87-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48d87-127">Minimum supported server</span></span><br/> | <span data-ttu-id="48d87-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48d87-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="48d87-129">標頭</span><span class="sxs-lookup"><span data-stu-id="48d87-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="48d87-130"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="48d87-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48d87-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48d87-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d87-132">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="48d87-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="48d87-133">多媒體操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="48d87-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





