---
title: WM_NCPOINTERUP 訊息
description: 在視窗的非工作區上建立連絡人的指標中斷連絡人時張貼。
ms.assetid: 4bdc11da-227c-4be1-bf0b-99704caa1322
keywords:
- WM_NCPOINTERUP 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_NCPOINTERUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: a875814b51558c20de47eeee525f6dd35f716fac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686176"
---
# <a name="wm_ncpointerup-message"></a><span data-ttu-id="6adb8-104">WM_NCPOINTERUP 訊息</span><span class="sxs-lookup"><span data-stu-id="6adb8-104">WM_NCPOINTERUP message</span></span>

<span data-ttu-id="6adb8-105">在視窗的非工作區上建立連絡人的指標中斷連絡人時張貼。</span><span class="sxs-lookup"><span data-stu-id="6adb8-105">Posted when a pointer that made contact over the non-client area of a window breaks contact.</span></span> <span data-ttu-id="6adb8-106">訊息會以指標所用的視窗為目標，而指標會在該視窗上以隱含方式捕捉至視窗，讓視窗繼續接收指標的輸入，直到它中斷連絡人為止，包括 **WM_NCPOINTERUP** 通知。</span><span class="sxs-lookup"><span data-stu-id="6adb8-106">The message targets the window over which the pointer makes contact and the pointer is, at that point, implicitly captured to the window so that the window continues to receive input for the pointer until it breaks contact, including the **WM_NCPOINTERUP** notification.</span></span>

<span data-ttu-id="6adb8-107">如果視窗已捕捉到此指標，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="6adb8-107">If a window has captured this pointer, this message is not posted.</span></span> <span data-ttu-id="6adb8-108">相反地， [**WM_POINTERUP**](wm-pointerup.md) 會張貼到已捕獲此指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="6adb8-108">Instead, a [**WM_POINTERUP**](wm-pointerup.md) is posted to the window that has captured this pointer.</span></span>

> <span data-ttu-id="6adb8-109">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="6adb8-109">\[!Important\]</span></span>  
> <span data-ttu-id="6adb8-110">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="6adb8-110">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="6adb8-111">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="6adb8-111">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="6adb8-112">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="6adb8-112">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="6adb8-113">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="6adb8-113">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_NCPOINTERUP               0x0243
```



## <a name="parameters"></a><span data-ttu-id="6adb8-114">參數</span><span class="sxs-lookup"><span data-stu-id="6adb8-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6adb8-115">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6adb8-115">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6adb8-116">包含指標識別碼和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="6adb8-116">Contains the pointer identifier and additional information.</span></span> <span data-ttu-id="6adb8-117">使用下列宏來取得此資訊。</span><span class="sxs-lookup"><span data-stu-id="6adb8-117">Use the following macros to retrieve this information.</span></span>

<span data-ttu-id="6adb8-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) (WPARAM) ：指標識別碼</span><span class="sxs-lookup"><span data-stu-id="6adb8-118">[**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api)(wParam): pointer identifier</span></span>

<span data-ttu-id="6adb8-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) (wParam) ：處理 [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) 訊息時所傳回的點擊測試值。</span><span class="sxs-lookup"><span data-stu-id="6adb8-119">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(wParam): hit-test value returned from processing the [**WM_NCHITTEST**](../inputdev/wm-nchittest.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="6adb8-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6adb8-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6adb8-121">包含指標的點位置。</span><span class="sxs-lookup"><span data-stu-id="6adb8-121">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="6adb8-122">因為指標可能會透過非一般區域與裝置聯繫，所以這個點位置可以簡化更複雜的指標區域。</span><span class="sxs-lookup"><span data-stu-id="6adb8-122">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="6adb8-123">如果可能的話，應用程式應該使用完整的指標區域資訊，而不是點位置。</span><span class="sxs-lookup"><span data-stu-id="6adb8-123">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="6adb8-124">您可以使用下列宏來取出點的實際螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="6adb8-124">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="6adb8-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) (LPARAM) ： X (水準點) 座標。</span><span class="sxs-lookup"><span data-stu-id="6adb8-125">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="6adb8-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam) (LPARAM) ： Y (垂直點) 座標。</span><span class="sxs-lookup"><span data-stu-id="6adb8-126">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6adb8-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="6adb8-127">Return value</span></span>

<span data-ttu-id="6adb8-128">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6adb8-128">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="6adb8-129">如果應用程式未處理此訊息，則應該呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="6adb8-129">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="6adb8-130">備註</span><span class="sxs-lookup"><span data-stu-id="6adb8-130">Remarks</span></span>

<span data-ttu-id="6adb8-131">如果應用程式未處理此訊息， [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) 可能會根據訊息中包含的點擊測試結果，執行一或多個系統動作。</span><span class="sxs-lookup"><span data-stu-id="6adb8-131">If the application does not process this message, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may perform one or more system actions depending on the hit-test result included in the message.</span></span> <span data-ttu-id="6adb8-132">一般而言，應用程式應該不需要處理此訊息。</span><span class="sxs-lookup"><span data-stu-id="6adb8-132">Typically, applications should not need to handle this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6adb8-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6adb8-133">Requirements</span></span>



| <span data-ttu-id="6adb8-134">需求</span><span class="sxs-lookup"><span data-stu-id="6adb8-134">Requirement</span></span> | <span data-ttu-id="6adb8-135">值</span><span class="sxs-lookup"><span data-stu-id="6adb8-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6adb8-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6adb8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6adb8-137">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6adb8-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6adb8-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6adb8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6adb8-139">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6adb8-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6adb8-140">標頭</span><span class="sxs-lookup"><span data-stu-id="6adb8-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6adb8-141"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="6adb8-141"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6adb8-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6adb8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6adb8-143">訊息</span><span class="sxs-lookup"><span data-stu-id="6adb8-143">Messages</span></span>](messages.md)
</dt> </dl>

 

