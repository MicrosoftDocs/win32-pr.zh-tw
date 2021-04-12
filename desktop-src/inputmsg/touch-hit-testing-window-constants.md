---
title: 觸控點擊測試視窗常數
description: 指出透過 RegisterTouchHitTestingWindow 函式註冊的 windows 會如何處理觸控點擊測試的訊息。
ms.assetid: CC6CCD0B-882F-4DA7-B886-D4BD18D6060C
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_DEFAULT
- TOUCH_HIT_TESTING_CLIENT
- TOUCH_HIT_TESTING_NONE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 46d577e03eaf918e4f2ea40aae30a2ab5112b630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385033"
---
# <a name="touch-hit-testing-window-constants"></a><span data-ttu-id="def2b-103">觸控點擊測試視窗常數</span><span class="sxs-lookup"><span data-stu-id="def2b-103">Touch Hit Testing Window Constants</span></span>

<span data-ttu-id="def2b-104">指出透過 [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) 函式註冊的 windows 會如何處理觸控點擊測試的訊息。</span><span class="sxs-lookup"><span data-stu-id="def2b-104">Indicates how messages for touch hit testing are processed by windows that are registered through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>



| <span data-ttu-id="def2b-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="def2b-105">Constant/value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="def2b-106">Description</span><span class="sxs-lookup"><span data-stu-id="def2b-106">Description</span></span>                                                                                                                            |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TOUCH_HIT_TESTING_DEFAULT"></span><span id="touch_hit_testing_default"></span><dl> <span data-ttu-id="def2b-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="def2b-107"><dt>**TOUCH_HIT_TESTING_DEFAULT**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="def2b-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) 的訊息不會傳送至目標視窗，而是傳送至子視窗。</span><span class="sxs-lookup"><span data-stu-id="def2b-108">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window but are sent to child windows.</span></span><br/> |
| <span id="TOUCH_HIT_TESTING_CLIENT"></span><span id="touch_hit_testing_client"></span><dl> <span data-ttu-id="def2b-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="def2b-109"><dt>**TOUCH_HIT_TESTING_CLIENT**</dt> <dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="def2b-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) 的訊息會傳送至目標視窗。</span><span class="sxs-lookup"><span data-stu-id="def2b-110">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are sent to the target window.</span></span><br/>                                   |
| <span id="TOUCH_HIT_TESTING_NONE"></span><span id="touch_hit_testing_none"></span><dl> <span data-ttu-id="def2b-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="def2b-111"><dt>**TOUCH_HIT_TESTING_NONE**</dt> <dt>2 (0x2)</dt></span></span> </dl>          | <span data-ttu-id="def2b-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) 的訊息不會傳送至目標視窗或子視窗。</span><span class="sxs-lookup"><span data-stu-id="def2b-112">[**WM_TOUCHHITTESTING**](wm-touchhittesting.md) messages are not sent to the target window or child windows.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="def2b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="def2b-113">Requirements</span></span>



| <span data-ttu-id="def2b-114">需求</span><span class="sxs-lookup"><span data-stu-id="def2b-114">Requirement</span></span> | <span data-ttu-id="def2b-115">值</span><span class="sxs-lookup"><span data-stu-id="def2b-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="def2b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="def2b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="def2b-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="def2b-117">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="def2b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="def2b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="def2b-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="def2b-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="def2b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="def2b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="def2b-121"><dt>Winuser。h</dt></span><span class="sxs-lookup"><span data-stu-id="def2b-121"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def2b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="def2b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def2b-123">常數</span><span class="sxs-lookup"><span data-stu-id="def2b-123">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="def2b-124">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="def2b-124">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

