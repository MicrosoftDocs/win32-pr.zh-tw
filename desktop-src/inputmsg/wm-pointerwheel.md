---
title: WM_POINTERWHEEL 訊息
description: 當滾動滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。
ms.assetid: 6eec37da-2200-4be1-bf0b-44704caa1320
keywords:
- WM_POINTERWHEEL 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_POINTERWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ad1177b2e92e47ca40c745e6cd5f1ea2cf259215
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464921"
---
# <a name="wm_pointerwheel-message"></a><span data-ttu-id="3fb9e-104">WM_POINTERWHEEL 訊息</span><span class="sxs-lookup"><span data-stu-id="3fb9e-104">WM_POINTERWHEEL message</span></span>

<span data-ttu-id="3fb9e-105">當滾動滾輪旋轉時，張貼至具有前景鍵盤焦點的視窗。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-105">Posted to the window with foreground keyboard focus when a scroll wheel is rotated.</span></span>

<span data-ttu-id="3fb9e-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="3fb9e-107">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="3fb9e-107">\[!Important\]</span></span>  
> <span data-ttu-id="3fb9e-108">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-108">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="3fb9e-109">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-109">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="3fb9e-110">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-110">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="3fb9e-111">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-111">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_POINTERWHEEL            0x024E
```



## <a name="parameters"></a><span data-ttu-id="3fb9e-112">參數</span><span class="sxs-lookup"><span data-stu-id="3fb9e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fb9e-113">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3fb9e-113">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fb9e-114">包含指標識別碼和輪子差異。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-114">Contains the pointer identifier and wheel delta.</span></span> <span data-ttu-id="3fb9e-115">使用下列宏來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-115">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="3fb9e-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-116">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier.</span></span>

<span data-ttu-id="3fb9e-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam) (WPARAM) ：滾輪 DELTA 作為帶正負號的簡短值。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-117">[**GET_WHEEL_DELTA_WPARAM**](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)(wParam): wheel delta as a signed short value.</span></span>

</dd> <dt>

<span data-ttu-id="3fb9e-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fb9e-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fb9e-119">包含指標的點位置。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-119">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="3fb9e-120">因為指標可能會透過非一般區域與裝置聯繫，所以這個點位置可以簡化更複雜的指標區域。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-120">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="3fb9e-121">如果可能的話，應用程式應該使用完整的指標區域資訊，而不是點位置。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-121">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="3fb9e-122">您可以使用下列宏來取出點的實際螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-122">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="3fb9e-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) (LPARAM) ： X (水準點) 座標。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-123">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="3fb9e-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam) (LPARAM) ： Y (垂直點) 座標。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-124">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fb9e-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fb9e-125">Return value</span></span>

<span data-ttu-id="3fb9e-126">如果應用程式處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-126">If the application processes this message, it should return zero.</span></span>

<span data-ttu-id="3fb9e-127">如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-127">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="3fb9e-128">備註</span><span class="sxs-lookup"><span data-stu-id="3fb9e-128">Remarks</span></span>

<span data-ttu-id="3fb9e-129">若要取出滾輪滾動單位，請使用呼叫 [**GetPointerInfo**](/previous-versions/windows/desktop/api)函數所傳回 [**POINTER_INFO**](/previous-versions/windows/desktop/api)結構的 **inputData** 。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-129">To retrieve the wheel scroll units, use the **inputData** filed of the [**POINTER_INFO**](/previous-versions/windows/desktop/api) structure returned by calling [**GetPointerInfo**](/previous-versions/windows/desktop/api) function.</span></span> <span data-ttu-id="3fb9e-130">此欄位包含帶正負號的值，並以 **WHEEL_DELTA** 的倍數表示。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-130">This field contains a signed value and is expressed in a multiple of **WHEEL_DELTA**.</span></span> <span data-ttu-id="3fb9e-131">正值表示向前旋轉，負數值表示向前旋轉。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-131">A positive value indicates a rotation forward and a negative value indicates a rotation backward.</span></span>

<span data-ttu-id="3fb9e-132">請注意，即使滑鼠游標位於應用程式視窗之外，也可以傳遞輪子輸入。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-132">Note that the wheel inputs may be delivered even if the mouse cursor is located outside of application s window.</span></span> <span data-ttu-id="3fb9e-133">滾輪訊息的傳遞方式與鍵盤輸入非常類似。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-133">The wheel messages are delivered in a way very similar to the keyboard inputs.</span></span> <span data-ttu-id="3fb9e-134">Foregournd 訊息佇列的焦點視窗會接收滾輪訊息。</span><span class="sxs-lookup"><span data-stu-id="3fb9e-134">The focus window of the foregournd message queue receives the wheel messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb9e-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fb9e-135">Requirements</span></span>



| <span data-ttu-id="3fb9e-136">需求</span><span class="sxs-lookup"><span data-stu-id="3fb9e-136">Requirement</span></span> | <span data-ttu-id="3fb9e-137">值</span><span class="sxs-lookup"><span data-stu-id="3fb9e-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb9e-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3fb9e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3fb9e-139">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fb9e-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="3fb9e-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3fb9e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3fb9e-141">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3fb9e-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3fb9e-142">標頭</span><span class="sxs-lookup"><span data-stu-id="3fb9e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fb9e-143"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="3fb9e-143"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb9e-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fb9e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb9e-145">訊息</span><span class="sxs-lookup"><span data-stu-id="3fb9e-145">Messages</span></span>](messages.md)
</dt> </dl>

 

