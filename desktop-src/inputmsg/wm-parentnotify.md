---
title: WM_PARENTNOTIFY 訊息
description: 當子系視窗發生重大動作時，傳送至視窗。
ms.assetid: 4bdc37da-227c-4be1-bf0b-99704caa1444
keywords:
- WM_PARENTNOTIFY 訊息輸入訊息和通知
topic_type:
- apiref
api_name:
- WM_PARENTNOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 2e19edf25933a035514f9c42b0da6014eccfdb0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508936"
---
# <a name="wm_parentnotify-message"></a><span data-ttu-id="4a8a4-104">WM_PARENTNOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="4a8a4-104">WM_PARENTNOTIFY message</span></span>

<span data-ttu-id="4a8a4-105">當子系視窗發生重大動作時，傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-105">Sent to a window when a significant action occurs on a descendant window.</span></span> <span data-ttu-id="4a8a4-106">這則訊息現在已擴充，以包含 [**WM_POINTERDOWN**](wm-pointerdown.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-106">This message is now extended to include the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span> <span data-ttu-id="4a8a4-107">建立子視窗時，系統會在建立視窗的 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)或 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)函式之前傳送 [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) 。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-107">When the child window is being created, the system sends [**WM_PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) just before the [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function that creates the window returns.</span></span> <span data-ttu-id="4a8a4-108">當子視窗被終結時，系統會先傳送訊息，然後再進行任何損毀視窗的處理。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-108">When the child window is being destroyed, the system sends the message before any processing to destroy the window takes place.</span></span>

<span data-ttu-id="4a8a4-109">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>

> <span data-ttu-id="4a8a4-110">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="4a8a4-110">\[!Important\]</span></span>  
> <span data-ttu-id="4a8a4-111">桌面應用程式應該要感知 DPI。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-111">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="4a8a4-112">如果您的應用程式不是 DPI 感知，指標訊息和相關結構中所包含的螢幕座標可能會因為 DPI 虛擬化而出現不正確的情況。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-112">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="4a8a4-113">DPI 虛擬化提供自動調整支援給非 DPI 感知的應用程式，而且預設為使用中 (使用者可以關閉) 。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-113">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="4a8a4-114">如需詳細資訊，請參閱 [撰寫高 DPI 的 Win32 應用程式](/previous-versions//dd464660(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-114">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_PARENTNOTIFY             0x0210
```



## <a name="parameters"></a><span data-ttu-id="4a8a4-115">參數</span><span class="sxs-lookup"><span data-stu-id="4a8a4-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a8a4-116">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a8a4-116">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a8a4-117">*WParam* 的低序位文字指定要通知其父代的事件。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-117">The low-order word of *wParam* specifies the event for which the parent is being notified.</span></span> <span data-ttu-id="4a8a4-118">高序位字的值取決於低序位字組的值。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-118">The value of the high-order word depends on the value of the low-order word.</span></span> <span data-ttu-id="4a8a4-119">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-119">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="4a8a4-120">LOWORD (*wParam*) </span><span class="sxs-lookup"><span data-stu-id="4a8a4-120">LOWORD(*wParam*)</span></span>                                                                                                                                                                                                             | <span data-ttu-id="4a8a4-121">意義</span><span class="sxs-lookup"><span data-stu-id="4a8a4-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WM_CREATE"></span><span id="wm_create"></span><dl> <span data-ttu-id="4a8a4-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-122"><dt>**WM_CREATE**</dt> <dt>0x0001</dt></span></span> </dl>                | <span data-ttu-id="4a8a4-123">正在建立子視窗。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-123">The child window is being created.</span></span><br/> <span data-ttu-id="4a8a4-124">HIWORD (*wParam*) 是子視窗的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-124">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="4a8a4-125">*lParam* 是子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-125">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WM_DESTROY"></span><span id="wm_destroy"></span><dl> <span data-ttu-id="4a8a4-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-126"><dt>**WM_DESTROY**</dt> <dt>0x0002</dt></span></span> </dl>             | <span data-ttu-id="4a8a4-127">正在終結子視窗。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-127">The child window is being destroyed.</span></span><br/> <span data-ttu-id="4a8a4-128">HIWORD (*wParam*) 是子視窗的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-128">HIWORD(*wParam*) is the identifier of the child window.</span></span><br/> <span data-ttu-id="4a8a4-129">*lParam* 是子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-129">*lParam* is a handle to the child window.</span></span><br/>                                                                                                                                                                                                                        |
| <span id="WM_LBUTTONDOWN"></span><span id="wm_lbuttondown"></span><dl> <span data-ttu-id="4a8a4-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-130"><dt>**WM_LBUTTONDOWN**</dt> <dt>0x0201</dt></span></span> </dl> | <span data-ttu-id="4a8a4-131">使用者已將游標放在子視窗上方，並已按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-131">The user has placed the cursor over the child window and has clicked the left mouse button.</span></span><br/> <span data-ttu-id="4a8a4-132">未定義 HIWORD (*wParam*) 。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-132">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="4a8a4-133">*lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-133">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                       |
| <span id="WM_MBUTTONDOWN"></span><span id="wm_mbuttondown"></span><dl> <span data-ttu-id="4a8a4-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-134"><dt>**WM_MBUTTONDOWN**</dt> <dt>0x0207</dt></span></span> </dl> | <span data-ttu-id="4a8a4-135">使用者已將游標放在子視窗上方，並已按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-135">The user has placed the cursor over the child window and has clicked the middle mouse button.</span></span><br/> <span data-ttu-id="4a8a4-136">未定義 HIWORD (*wParam*) 。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-136">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="4a8a4-137">*lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-137">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                     |
| <span id="WM_RBUTTONDOWN"></span><span id="wm_rbuttondown"></span><dl> <span data-ttu-id="4a8a4-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-138"><dt>**WM_RBUTTONDOWN**</dt> <dt>0x0204</dt></span></span> </dl> | <span data-ttu-id="4a8a4-139">使用者將游標放在子視窗上方，然後按一下滑鼠右鍵。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-139">The user has placed the cursor over the child window and has clicked the right mouse button.</span></span><br/> <span data-ttu-id="4a8a4-140">未定義 HIWORD (*wParam*) 。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-140">HIWORD(*wParam*) is undefined.</span></span><br/> <span data-ttu-id="4a8a4-141">*lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-141">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/>                                                                                                      |
| <span id="WM_XBUTTONDOWN"></span><span id="wm_xbuttondown"></span><dl> <span data-ttu-id="4a8a4-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-142"><dt>**WM_XBUTTONDOWN**</dt> <dt>0x020B</dt></span></span> </dl> | <span data-ttu-id="4a8a4-143">使用者已將游標放在子視窗上方，並已按一下第一個或第二個 X 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-143">The user has placed the cursor over the child window and has clicked the first or second X button.</span></span><br/> <span data-ttu-id="4a8a4-144">HIWORD (*wParam*) 指出已按下的按鈕。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-144">HIWORD(*wParam*) indicates which button was pressed.</span></span> <span data-ttu-id="4a8a4-145">此參數可以是下列其中一個值： XBUTTON1 或 XBUTTON2。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-145">This parameter can be one of the following values: XBUTTON1 or XBUTTON2.</span></span><br/> <span data-ttu-id="4a8a4-146">*lParam* 是資料指標的 x 座標是低序位字組，而游標的 y 座標則是高序位單字。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-146">*lParam* is the x-coordinate of the cursor is the low-order word, and the y-coordinate of the cursor is the high-order word.</span></span><br/> |
| <span id="WM_POINTERDOWN"></span><span id="wm_pointerdown"></span><dl> <span data-ttu-id="4a8a4-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-147"><dt>**WM_POINTERDOWN**</dt> <dt>0x0246</dt></span></span> </dl> | <span data-ttu-id="4a8a4-148">指標已與子視窗建立聯繫。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-148">A pointer has made contact with the child window.</span></span><br/> <span data-ttu-id="4a8a4-149">HIWORD (*wParam*) 包含產生 [**WM_POINTERDOWN**](wm-pointerdown.md) 事件之指標的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-149">HIWORD(*wParam*) contains the identifier of the pointer that generated the [**WM_POINTERDOWN**](wm-pointerdown.md) event.</span></span><br/>                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="4a8a4-150">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a8a4-150">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a8a4-151">包含指標的點位置。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-151">Contains the point location of the pointer.</span></span>

> [!Note]  
> <span data-ttu-id="4a8a4-152">因為指標可能會透過非一般區域與裝置聯繫，所以這個點位置可以簡化更複雜的指標區域。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-152">Because the pointer may make contact with the device over a non-trivial area, this point location may be a simplification of a more complex pointer area.</span></span> <span data-ttu-id="4a8a4-153">如果可能的話，應用程式應該使用完整的指標區域資訊，而不是點位置。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-153">Whenever possible, an application should use the complete pointer area information instead of the point location.</span></span>

 

<span data-ttu-id="4a8a4-154">您可以使用下列宏來取出點的實際螢幕座標。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-154">Use the following macros to retrieve the physical screen coordinates of the point.</span></span>

-   <span data-ttu-id="4a8a4-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam) (LPARAM) ： X (水準點) 座標。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-155">[**GET_X_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_x_lparam)(lParam): the x (horizontal point) coordinate.</span></span>
-   <span data-ttu-id="4a8a4-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam) (LPARAM) ： Y (垂直點) 座標。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-156">[**GET_Y_LPARAM**](/windows/win32/api/windowsx/nf-windowsx-get_y_lparam)(lParam): the y (vertical point) coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a8a4-157">傳回值</span><span class="sxs-lookup"><span data-stu-id="4a8a4-157">Return value</span></span>

<span data-ttu-id="4a8a4-158">如果應用程式處理此訊息，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-158">If the application processes this message, it returns zero.</span></span>

<span data-ttu-id="4a8a4-159">如果應用程式未處理此訊息，則會呼叫 [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-159">If the application does not process this message, it calls [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a8a4-160">備註</span><span class="sxs-lookup"><span data-stu-id="4a8a4-160">Remarks</span></span>

<span data-ttu-id="4a8a4-161">此訊息也會傳送至子視窗的所有上階視窗，包括最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-161">This message is also sent to all ancestor windows of the child window, including the top-level window.</span></span>

<span data-ttu-id="4a8a4-162">除了具有 **WS_EX_NOPARENTNOTIFY** 延伸視窗樣式以外的所有子視窗，會將此訊息傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-162">All child windows, except those that have the **WS_EX_NOPARENTNOTIFY** extended window style, send this message to their parent windows.</span></span> <span data-ttu-id="4a8a4-163">依預設，對話方塊中的子視窗會有 **WS_EX_NOPARENTNOTIFY** 樣式，除非呼叫 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式來建立沒有此樣式的子視窗。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-163">By default, child windows in a dialog box have the **WS_EX_NOPARENTNOTIFY** style, unless the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function is called to create the child window without this style.</span></span>

<span data-ttu-id="4a8a4-164">此通知可讓子視窗的上階視窗有機會檢查指標資訊，並且在必要時使用指標捕捉函式來捕捉指標。</span><span class="sxs-lookup"><span data-stu-id="4a8a4-164">This notification provides the child window's ancestor windows an opportunity to examine the pointer information and, if required, capture the pointer using the pointer capture functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a8a4-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a8a4-165">Requirements</span></span>



| <span data-ttu-id="4a8a4-166">需求</span><span class="sxs-lookup"><span data-stu-id="4a8a4-166">Requirement</span></span> | <span data-ttu-id="4a8a4-167">值</span><span class="sxs-lookup"><span data-stu-id="4a8a4-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8a4-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a8a4-168">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8a4-169">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a8a4-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="4a8a4-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a8a4-170">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8a4-171">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a8a4-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4a8a4-172">標頭</span><span class="sxs-lookup"><span data-stu-id="4a8a4-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a8a4-173"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4a8a4-173"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a8a4-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a8a4-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8a4-175">訊息</span><span class="sxs-lookup"><span data-stu-id="4a8a4-175">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="4a8a4-176">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-176">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="4a8a4-177">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-177">**CreateWindowEx**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

<span data-ttu-id="4a8a4-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a8a4-178">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="4a8a4-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4a8a4-179">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4a8a4-180">**WM_CREATE**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-180">**WM_CREATE**</span></span>](../winmsg/wm-create.md)
</dt> <dt>

[<span data-ttu-id="4a8a4-181">**WM_DESTROY**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-181">**WM_DESTROY**</span></span>](../winmsg/wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="4a8a4-182">**WM_LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-182">**WM_LBUTTONDOWN**</span></span>](../inputdev/wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="4a8a4-183">**WM_MBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-183">**WM_MBUTTONDOWN**</span></span>](../inputdev/wm-mbuttondown.md)
</dt> <dt>

[<span data-ttu-id="4a8a4-184">**WM_RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-184">**WM_RBUTTONDOWN**</span></span>](../inputdev/wm-rbuttondown.md)
</dt> <dt>

[<span data-ttu-id="4a8a4-185">**WM_XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="4a8a4-185">**WM_XBUTTONDOWN**</span></span>](../inputdev/wm-xbuttondown.md)
</dt> </dl>

 

