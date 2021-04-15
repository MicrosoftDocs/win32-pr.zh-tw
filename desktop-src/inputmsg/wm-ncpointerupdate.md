---
title: WM_NCPOINTERUPDATE 訊息
description: 張貼以提供指標的更新，以在視窗的非工作區上建立連絡人，或是當滑鼠停留 uncaptured 連絡人在視窗的非工作區上移動時。
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUPDATE 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_NCPOINTERUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 09ef5fd6f3b7378a963be4278f1fabdf0f6ab351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384413"
---
# <a name="wm_ncpointerupdate-message"></a><span data-ttu-id="e2cde-104">WM_NCPOINTERUPDATE 訊息</span><span class="sxs-lookup"><span data-stu-id="e2cde-104">WM_NCPOINTERUPDATE message</span></span>

<span data-ttu-id="e2cde-105">張貼以提供指標的更新，以在視窗的非工作區上建立連絡人，或是當滑鼠停留 uncaptured 連絡人在視窗的非工作區上移動時。</span><span class="sxs-lookup"><span data-stu-id="e2cde-105">Posted to provide an update on a pointer that made contact over the non-client area of a window or when a hovering uncaptured contact moves over the non-client area of a window.</span></span> <span data-ttu-id="e2cde-106">當指標停留時，訊息會以指標發生的任何視窗為目標。</span><span class="sxs-lookup"><span data-stu-id="e2cde-106">While the pointer is hovering, the message targets whichever window the pointer happens to be over.</span></span> <span data-ttu-id="e2cde-107">當指標與介面聯繫時，指標就會隱含地捕捉到指標所變成的視窗，而該視窗會繼續接收指標的輸入，直到中斷連絡人為止。</span><span class="sxs-lookup"><span data-stu-id="e2cde-107">While the pointer is in contact with the surface, the pointer is implicitly captured to the window over which the pointer made contact and that window continues to receive input for the pointer until it breaks contact.</span></span>

<span data-ttu-id="e2cde-108">如果視窗已捕捉到此指標，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2cde-108">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="e2cde-109">相反地， [**WM_POINTERUPDATE**](wm-pointerupdate.md) 會張貼到已捕獲此指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="e2cde-109">Instead, a [**WM_POINTERUPDATE**](wm-pointerupdate.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="e2cde-110">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="e2cde-110">\[!Important\]</span></span>  
> <span data-ttu-id="e2cde-111">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="e2cde-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="e2cde-112">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="e2cde-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="e2cde-113">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="e2cde-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="e2cde-114">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="e2cde-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUPDATE                 0x0241
```



## <a name="parameters"></a><span data-ttu-id="e2cde-115">參數</span><span class="sxs-lookup"><span data-stu-id="e2cde-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2cde-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e2cde-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2cde-117">包含指標識別碼和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="e2cde-117">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="e2cde-118">使用下列宏來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="e2cde-118">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="e2cde-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼</span><span class="sxs-lookup"><span data-stu-id="e2cde-119">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="e2cde-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (wParam) ：處理 [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) 訊息時所傳回的點擊測試值。</span><span class="sxs-lookup"><span data-stu-id="e2cde-120">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="e2cde-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e2cde-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e2cde-122">包含指標的點位置。</span><span class="sxs-lookup"><span data-stu-id="e2cde-122">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="e2cde-123">因為指標可能會透過非一般區域與裝置聯繫，所以這個點位置可以簡化更複雜的指標區域。</span><span class="sxs-lookup"><span data-stu-id="e2cde-123">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="e2cde-124">如果可能的話，應用程式應該使用完整的指標區域資訊，而不是點位置。</span><span class="sxs-lookup"><span data-stu-id="e2cde-124">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="e2cde-125">您可以使用下列宏來取出點的實際螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="e2cde-125">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="e2cde-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) (LPARAM) ： X (水準點) 座標。</span><span class="sxs-lookup"><span data-stu-id="e2cde-126">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="e2cde-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam) (LPARAM) ： Y (垂直點) 座標。</span><span class="sxs-lookup"><span data-stu-id="e2cde-127">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2cde-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2cde-128">Return value</span></span>

<span data-ttu-id="e2cde-129">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e2cde-129">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="e2cde-130">如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="e2cde-130">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2cde-131">備註</span><span class="sxs-lookup"><span data-stu-id="e2cde-131">Remarks</span></span>

<span data-ttu-id="e2cde-132">如果應用程式未處理此訊息， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 可能會根據訊息中包含的點擊測試結果，執行一或多個系統動作。</span><span class="sxs-lookup"><span data-stu-id="e2cde-132">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="e2cde-133">一般而言，應用程式應該不需要處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="e2cde-133">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2cde-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2cde-134">Requirements</span></span>



| <span data-ttu-id="e2cde-135">需求</span><span class="sxs-lookup"><span data-stu-id="e2cde-135">Requirement</span></span> | <span data-ttu-id="e2cde-136">值</span><span class="sxs-lookup"><span data-stu-id="e2cde-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2cde-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2cde-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e2cde-138">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2cde-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e2cde-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2cde-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e2cde-140">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2cde-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e2cde-141">標頭</span><span class="sxs-lookup"><span data-stu-id="e2cde-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2cde-142"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="e2cde-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2cde-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2cde-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2cde-144">訊息</span><span class="sxs-lookup"><span data-stu-id="e2cde-144">Messages</span></span>](messages.md)
</dt> </dl>

 

