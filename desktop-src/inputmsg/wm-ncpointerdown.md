---
title: WM_NCPOINTERDOWN 訊息
description: 當指標在視窗的非工作區上進行聯繫時公佈。
ms.assetid: 3bdc37da-217c-4be1-bf0b-99704bda1322
keywords:
- WM_NCPOINTERDOWN 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_NCPOINTERDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 6f4c3ef8ed75c5bd29250cd2f9ce4d666b6d961d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934745"
---
# <a name="wm_ncpointerdown-message"></a><span data-ttu-id="6f16a-104">WM_NCPOINTERDOWN 訊息</span><span class="sxs-lookup"><span data-stu-id="6f16a-104">WM_NCPOINTERDOWN message</span></span>

<span data-ttu-id="6f16a-105">當指標在視窗的非工作區上進行聯繫時公佈。</span><span class="sxs-lookup"><span data-stu-id="6f16a-105">Posted when a pointer makes contact over the non-client area of a window.</span></span> <span data-ttu-id="6f16a-106">訊息會以指標所要接觸的視窗為目標。</span><span class="sxs-lookup"><span data-stu-id="6f16a-106">The message targets the window over which the pointer makes contact.</span></span> <span data-ttu-id="6f16a-107">指標會隱含地捕捉至視窗，讓視窗繼續接收指標的輸入，直到它中斷 contact 為止。</span><span class="sxs-lookup"><span data-stu-id="6f16a-107">The pointer is implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="6f16a-108">如果視窗已捕捉到此指標，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="6f16a-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="6f16a-109">相反地， [**WM_POINTERDOWN**](wm-pointerdown.md) 會張貼到已捕獲此指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="6f16a-109">Instead, a [**WM_POINTERDOWN**](wm-pointerdown.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="6f16a-110">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="6f16a-110">\[!Important\]</span></span>  
> <span data-ttu-id="6f16a-111">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="6f16a-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="6f16a-112">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="6f16a-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="6f16a-113">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="6f16a-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="6f16a-114">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6f16a-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERDOWN                 0x0242
```



## <a name="parameters"></a><span data-ttu-id="6f16a-115">參數</span><span class="sxs-lookup"><span data-stu-id="6f16a-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f16a-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f16a-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f16a-117">包含指標識別碼和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6f16a-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="6f16a-118">使用下列宏來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="6f16a-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="6f16a-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f16a-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="6f16a-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (wParam) ：處理 [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) 訊息時所傳回的點擊測試值。</span><span class="sxs-lookup"><span data-stu-id="6f16a-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6f16a-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f16a-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f16a-122">包含指標的點位置。</span><span class="sxs-lookup"><span data-stu-id="6f16a-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="6f16a-123">因為指標可能會透過非一般區域與裝置聯繫，所以這個點位置可以簡化更複雜的指標區域。</span><span class="sxs-lookup"><span data-stu-id="6f16a-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="6f16a-124">如果可能的話，應用程式應該使用完整的指標區域資訊，而不是點位置。</span><span class="sxs-lookup"><span data-stu-id="6f16a-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="6f16a-125">您可以使用下列宏來取出點的實際螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="6f16a-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="6f16a-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) (LPARAM) ： X (水準點) 座標。</span><span class="sxs-lookup"><span data-stu-id="6f16a-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="6f16a-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam) (LPARAM) ： Y (垂直點) 座標。</span><span class="sxs-lookup"><span data-stu-id="6f16a-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f16a-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f16a-128">Return value</span></span>

<span data-ttu-id="6f16a-129">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6f16a-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="6f16a-130">如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="6f16a-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="6f16a-131">備註</span><span class="sxs-lookup"><span data-stu-id="6f16a-131">Remarks</span></span>

<span data-ttu-id="6f16a-132">如果應用程式未處理此訊息， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 可能會根據訊息中包含的點擊測試結果，執行一或多個系統動作。</span><span class="sxs-lookup"><span data-stu-id="6f16a-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="6f16a-133">一般而言，應用程式應該不需要處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="6f16a-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f16a-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f16a-134">Requirements</span></span>



| <span data-ttu-id="6f16a-135">需求</span><span class="sxs-lookup"><span data-stu-id="6f16a-135">Requirement</span></span> | <span data-ttu-id="6f16a-136">值</span><span class="sxs-lookup"><span data-stu-id="6f16a-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f16a-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f16a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6f16a-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f16a-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6f16a-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f16a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6f16a-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f16a-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f16a-141">標頭</span><span class="sxs-lookup"><span data-stu-id="6f16a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f16a-142"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6f16a-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f16a-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f16a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f16a-144">訊息</span><span class="sxs-lookup"><span data-stu-id="6f16a-144">Messages</span></span>](messages.md)
</dt> </dl>

 

