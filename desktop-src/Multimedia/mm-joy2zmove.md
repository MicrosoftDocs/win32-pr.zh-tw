---
title: 'MM_JOY2ZMOVE 訊息 (Mmsystem .h) '
description: MM \_ JOY2ZMOVE 訊息會通知視窗，該視窗已捕捉至 Z 軸上的搖桿位置已變更的搖桿 JOYSTICKID2。
ms.assetid: f09a1a11-8c97-4a03-a388-8bf9ab89a3db
keywords:
- MM_JOY2ZMOVE message Windows 多媒體
topic_type:
- apiref
api_name:
- MM_JOY2ZMOVE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d899a4a1c93304075cb166ba805367ceed6ddd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106998033"
---
# <a name="mm_joy2zmove-message"></a><span data-ttu-id="89284-104">MM \_ JOY2ZMOVE 訊息</span><span class="sxs-lookup"><span data-stu-id="89284-104">MM\_JOY2ZMOVE message</span></span>

<span data-ttu-id="89284-105">**MM \_ JOY2ZMOVE** 訊息會通知視窗，該視窗已捕捉至 Z 軸上的搖桿位置已變更的搖桿 JOYSTICKID2。</span><span class="sxs-lookup"><span data-stu-id="89284-105">The **MM\_JOY2ZMOVE** message notifies the window that has captured joystick JOYSTICKID2 that the joystick position on the z-axis has changed.</span></span>


```C++
MM_JOY2ZMOVE 
fwButtons = wParam; 
zPos = LOWORD(lParam); 
```



## <a name="parameters"></a><span data-ttu-id="89284-106">參數</span><span class="sxs-lookup"><span data-stu-id="89284-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89284-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span><span class="sxs-lookup"><span data-stu-id="89284-107"><span id="fwButtons"></span><span id="fwbuttons"></span><span id="FWBUTTONS"></span>*fwButtons*</span></span>
</dt> <dd>

<span data-ttu-id="89284-108">識別按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="89284-108">Identifies the buttons that are pressed.</span></span> <span data-ttu-id="89284-109">它可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="89284-109">It can be one or more of the following values.</span></span>



| <span data-ttu-id="89284-110">需求</span><span class="sxs-lookup"><span data-stu-id="89284-110">Requirement</span></span> | <span data-ttu-id="89284-111">值</span><span class="sxs-lookup"><span data-stu-id="89284-111">Value</span></span> |
|--------------|------------------------------------|
| <span data-ttu-id="89284-112">歡樂 \_ BUTTON1</span><span class="sxs-lookup"><span data-stu-id="89284-112">JOY\_BUTTON1</span></span> | <span data-ttu-id="89284-113">第一個搖桿按鈕已按下。</span><span class="sxs-lookup"><span data-stu-id="89284-113">First joystick button is pressed.</span></span>  |
| <span data-ttu-id="89284-114">歡樂 \_ BUTTON2</span><span class="sxs-lookup"><span data-stu-id="89284-114">JOY\_BUTTON2</span></span> | <span data-ttu-id="89284-115">按下第二個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="89284-115">Second joystick button is pressed.</span></span> |
| <span data-ttu-id="89284-116">歡樂 \_ BUTTON3</span><span class="sxs-lookup"><span data-stu-id="89284-116">JOY\_BUTTON3</span></span> | <span data-ttu-id="89284-117">按下第三個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="89284-117">Third joystick button is pressed.</span></span>  |
| <span data-ttu-id="89284-118">歡樂 \_ BUTTON4</span><span class="sxs-lookup"><span data-stu-id="89284-118">JOY\_BUTTON4</span></span> | <span data-ttu-id="89284-119">按第四個操縱杆按鈕。</span><span class="sxs-lookup"><span data-stu-id="89284-119">Fourth joystick button is pressed.</span></span> |



 

</dd> <dt>

<span data-ttu-id="89284-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span><span class="sxs-lookup"><span data-stu-id="89284-120"><span id="zPos"></span><span id="zpos"></span><span id="ZPOS"></span>*zPos*</span></span>
</dt> <dd>

<span data-ttu-id="89284-121">搖桿的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="89284-121">The z-coordinate of the joystick.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="89284-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="89284-122">Requirements</span></span>



| <span data-ttu-id="89284-123">需求</span><span class="sxs-lookup"><span data-stu-id="89284-123">Requirement</span></span> | <span data-ttu-id="89284-124">值</span><span class="sxs-lookup"><span data-stu-id="89284-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89284-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89284-125">Minimum supported client</span></span><br/> | <span data-ttu-id="89284-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89284-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89284-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89284-127">Minimum supported server</span></span><br/> | <span data-ttu-id="89284-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89284-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89284-129">標頭</span><span class="sxs-lookup"><span data-stu-id="89284-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="89284-130"><dt>Mmsystem (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="89284-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89284-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89284-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89284-132">操縱 杆</span><span class="sxs-lookup"><span data-stu-id="89284-132">Joysticks</span></span>](joysticks.md)
</dt> <dt>

[<span data-ttu-id="89284-133">多媒體操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="89284-133">Multimedia Joystick Messages</span></span>](multimedia-joystick-messages.md)
</dt> </dl>

 

 





