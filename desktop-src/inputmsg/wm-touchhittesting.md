---
title: WM_TOUCHHITTESTING 訊息
description: 傳送至觸控下的視窗，以便判斷最可能的觸控目標。
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- WM_TOUCHHITTESTING 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104556"
---
# <a name="wm_touchhittesting-message"></a><span data-ttu-id="c4c82-104">WM_TOUCHHITTESTING 訊息</span><span class="sxs-lookup"><span data-stu-id="c4c82-104">WM_TOUCHHITTESTING message</span></span>

<span data-ttu-id="c4c82-105">傳送至觸控下的視窗，以便判斷最可能的觸控目標。</span><span class="sxs-lookup"><span data-stu-id="c4c82-105">Sent to a window on a touch down in order to determine the most probable touch target.</span></span>

> <span data-ttu-id="c4c82-106">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="c4c82-106">\[!Important\]</span></span>  
> <span data-ttu-id="c4c82-107">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="c4c82-107">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="c4c82-108">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="c4c82-108">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="c4c82-109">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="c4c82-109">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="c4c82-110">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c4c82-110">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a><span data-ttu-id="c4c82-111">參數</span><span class="sxs-lookup"><span data-stu-id="c4c82-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c82-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4c82-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4c82-113">未使用的。</span><span class="sxs-lookup"><span data-stu-id="c4c82-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="c4c82-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4c82-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4c82-115">包含觸控連絡人區域資料的 [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="c4c82-115">Pointer to the [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) structure that holds the touch contact area data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c82-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4c82-116">Return value</span></span>

<span data-ttu-id="c4c82-117">如果有一或多個元素位於觸控連絡人區域內，應用程式應該會傳回 [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)的結果。</span><span class="sxs-lookup"><span data-stu-id="c4c82-117">If one or more elements are within the touch contact area, an application should return the result of [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span></span>

<span data-ttu-id="c4c82-118">如果 touch contact 區域內沒有任何專案，則應用程式應該將 [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation)中的 **分數** 值設定為 [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) ，然後呼叫 [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation)來取得 LRESULT 傳回值。</span><span class="sxs-lookup"><span data-stu-id="c4c82-118">If no elements are within the touch contact area, an application should set the value of **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) to [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) and call [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) to get the LRESULT return value.</span></span>

<span data-ttu-id="c4c82-119">如果應用程式未處理此訊息，則必須呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="c4c82-119">If the application does not process this message, it must call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c82-120">備註</span><span class="sxs-lookup"><span data-stu-id="c4c82-120">Remarks</span></span>

<span data-ttu-id="c4c82-121">這則訊息會傳送至透過 [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) 函式註冊的 windows。</span><span class="sxs-lookup"><span data-stu-id="c4c82-121">This message is sent to windows that register through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c82-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4c82-122">Requirements</span></span>



| <span data-ttu-id="c4c82-123">需求</span><span class="sxs-lookup"><span data-stu-id="c4c82-123">Requirement</span></span> | <span data-ttu-id="c4c82-124">值</span><span class="sxs-lookup"><span data-stu-id="c4c82-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c82-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c4c82-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c82-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4c82-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="c4c82-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c4c82-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c82-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c4c82-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c4c82-129">標頭</span><span class="sxs-lookup"><span data-stu-id="c4c82-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c82-130"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="c4c82-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c82-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4c82-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c82-132">訊息</span><span class="sxs-lookup"><span data-stu-id="c4c82-132">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="c4c82-133">**觸控點擊測試分數**</span><span class="sxs-lookup"><span data-stu-id="c4c82-133">**Touch Hit Testing Scores**</span></span>](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

