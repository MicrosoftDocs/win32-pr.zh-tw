---
title: 'WM_VSCROLL 訊息 (Winuser .h) '
description: '\_當捲軸事件發生在視窗的標準垂直捲動條時，會將 WM VSCROLL 訊息傳送至視窗。'
ms.assetid: 495733b8-1aac-4ff7-b0be-15f14581f41c
keywords:
- WM_VSCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- WM_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12c83888b83e0d5f8d3c77775347ccc9b43a59d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106152"
---
# <a name="wm_vscroll-message"></a><span data-ttu-id="ad400-104">WM \_ VSCROLL 訊息</span><span class="sxs-lookup"><span data-stu-id="ad400-104">WM\_VSCROLL message</span></span>

<span data-ttu-id="ad400-105">當捲軸事件發生在視窗的標準垂直捲動條時，會將 **WM \_ VSCROLL** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="ad400-105">The **WM\_VSCROLL** message is sent to a window when a scroll event occurs in the window's standard vertical scroll bar.</span></span> <span data-ttu-id="ad400-106">當控制項中發生滾動事件時，此訊息也會傳送給垂直捲動條控制項的擁有者。</span><span class="sxs-lookup"><span data-stu-id="ad400-106">This message is also sent to the owner of a vertical scroll bar control when a scroll event occurs in the control.</span></span>

<span data-ttu-id="ad400-107">視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="ad400-107">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_VSCROLL

    WPARAM wParam
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ad400-108">參數</span><span class="sxs-lookup"><span data-stu-id="ad400-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad400-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ad400-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad400-110">如果 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 sb THUMBPOSITION 或 sb THUMBTRACK， [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定捲動方塊的目前位置 \_ \_ ; 否則，就不會使用這個字。</span><span class="sxs-lookup"><span data-stu-id="ad400-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the current position of the scroll box if the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is SB\_THUMBPOSITION or SB\_THUMBTRACK; otherwise, this word is not used.</span></span>

<span data-ttu-id="ad400-111">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定捲軸值，指出使用者的滾動要求。</span><span class="sxs-lookup"><span data-stu-id="ad400-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies a scroll bar value that indicates the user's scrolling request.</span></span> <span data-ttu-id="ad400-112">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ad400-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="ad400-113">值</span><span class="sxs-lookup"><span data-stu-id="ad400-113">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="ad400-114">意義</span><span class="sxs-lookup"><span data-stu-id="ad400-114">Meaning</span></span>                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <span data-ttu-id="ad400-115"><dt>**SB \_ 底部**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-115"><dt>**SB\_BOTTOM**</dt></span></span> </dl>                      | <span data-ttu-id="ad400-116">滾動至右下角。</span><span class="sxs-lookup"><span data-stu-id="ad400-116">Scrolls to the lower right.</span></span><br/>                                                                                                                                                                                    |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <span data-ttu-id="ad400-117"><dt>**SB \_ ENDSCROLL**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-117"><dt>**SB\_ENDSCROLL**</dt></span></span> </dl>             | <span data-ttu-id="ad400-118">結束滾動。</span><span class="sxs-lookup"><span data-stu-id="ad400-118">Ends scroll.</span></span><br/>                                                                                                                                                                                                   |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <span data-ttu-id="ad400-119"><dt>**SB \_ LINEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-119"><dt>**SB\_LINEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="ad400-120">向下滾動一行。</span><span class="sxs-lookup"><span data-stu-id="ad400-120">Scrolls one line down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <span data-ttu-id="ad400-121"><dt>**SB \_ 系列**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-121"><dt>**SB\_LINEUP**</dt></span></span> </dl>                      | <span data-ttu-id="ad400-122">向上滾動一行。</span><span class="sxs-lookup"><span data-stu-id="ad400-122">Scrolls one line up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <span data-ttu-id="ad400-123"><dt>**SB \_ PAGEDOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-123"><dt>**SB\_PAGEDOWN**</dt></span></span> </dl>                | <span data-ttu-id="ad400-124">向下滾動一個頁面。</span><span class="sxs-lookup"><span data-stu-id="ad400-124">Scrolls one page down.</span></span><br/>                                                                                                                                                                                         |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <span data-ttu-id="ad400-125"><dt>**SB \_ PAGEUP**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-125"><dt>**SB\_PAGEUP**</dt></span></span> </dl>                      | <span data-ttu-id="ad400-126">向上滾動一頁。</span><span class="sxs-lookup"><span data-stu-id="ad400-126">Scrolls one page up.</span></span><br/>                                                                                                                                                                                           |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <span data-ttu-id="ad400-127"><dt>**SB \_ THUMBPOSITION**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-127"><dt>**SB\_THUMBPOSITION**</dt></span></span> </dl> | <span data-ttu-id="ad400-128">使用者已拖曳捲動方塊 (thumb) 並放開滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="ad400-128">The user has dragged the scroll box (thumb) and released the mouse button.</span></span> <span data-ttu-id="ad400-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))表示捲動方塊在拖曳作業結束時的位置。</span><span class="sxs-lookup"><span data-stu-id="ad400-129">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position of the scroll box at the end of the drag operation.</span></span><br/>                          |
| <span id="SB_THUMBTRACK"></span><span id="sb_thumbtrack"></span><dl> <span data-ttu-id="ad400-130"><dt>**SB \_ THUMBTRACK**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-130"><dt>**SB\_THUMBTRACK**</dt></span></span> </dl>          | <span data-ttu-id="ad400-131">使用者正在拖曳捲軸方塊。</span><span class="sxs-lookup"><span data-stu-id="ad400-131">The user is dragging the scroll box.</span></span> <span data-ttu-id="ad400-132">這則訊息會重複傳送，直到使用者放開滑鼠按鍵為止。</span><span class="sxs-lookup"><span data-stu-id="ad400-132">This message is sent repeatedly until the user releases the mouse button.</span></span> <span data-ttu-id="ad400-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))表示捲動方塊拖曳至的位置。</span><span class="sxs-lookup"><span data-stu-id="ad400-133">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) indicates the position that the scroll box has been dragged to.</span></span><br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <span data-ttu-id="ad400-134"><dt>**SB \_ TOP**</dt></span><span class="sxs-lookup"><span data-stu-id="ad400-134"><dt>**SB\_TOP**</dt></span></span> </dl>                               | <span data-ttu-id="ad400-135">滾動至左上方。</span><span class="sxs-lookup"><span data-stu-id="ad400-135">Scrolls to the upper left.</span></span><br/>                                                                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="ad400-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ad400-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ad400-137">如果訊息是由捲軸控制項傳送，這個參數就是捲軸控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ad400-137">If the message is sent by a scroll bar control, this parameter is the handle to the scroll bar control.</span></span> <span data-ttu-id="ad400-138">如果訊息是由標準捲軸傳送，此參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ad400-138">If the message is sent by a standard scroll bar, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad400-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad400-139">Return value</span></span>

<span data-ttu-id="ad400-140">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="ad400-140">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad400-141">備註</span><span class="sxs-lookup"><span data-stu-id="ad400-141">Remarks</span></span>

<span data-ttu-id="ad400-142">\_當使用者拖曳捲動方塊時，應用程式通常會使用 SB THUMBTRACK 要求碼來提供意見反應。</span><span class="sxs-lookup"><span data-stu-id="ad400-142">The SB\_THUMBTRACK request code is typically used by applications that provide feedback as the user drags the scroll box.</span></span>

<span data-ttu-id="ad400-143">如果應用程式會滾動視窗的內容，則也必須使用 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) 函數重設捲動方塊的位置。</span><span class="sxs-lookup"><span data-stu-id="ad400-143">If an application scrolls the content of the window, it must also reset the position of the scroll box by using the [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) function.</span></span>

<span data-ttu-id="ad400-144">請注意， **WM \_ VSCROLL** 訊息只會攜帶16位的捲動方塊位置資料。</span><span class="sxs-lookup"><span data-stu-id="ad400-144">Note that the **WM\_VSCROLL** message carries only 16 bits of scroll box position data.</span></span> <span data-ttu-id="ad400-145">因此，僅依賴 **WM \_ VSCROLL** 的應用程式 (，以及用於捲軸位置資料之 [**wm \_ HSCROLL**](wm-hscroll.md)) 的應用程式，其實際最大位置值為65535。</span><span class="sxs-lookup"><span data-stu-id="ad400-145">Thus, applications that rely solely on **WM\_VSCROLL** (and [**WM\_HSCROLL**](wm-hscroll.md)) for scroll position data have a practical maximum position value of 65,535.</span></span>

<span data-ttu-id="ad400-146">不過，由於 [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)、 [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)、 [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)、 [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)、 [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)和 [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) 函數支援32位捲軸位置資料，因此可以規避 [**wm \_ HSCROLL**](wm-hscroll.md) 和 **wm \_ VSCROLL** 訊息的16位屏障。</span><span class="sxs-lookup"><span data-stu-id="ad400-146">However, because the [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos), [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange), [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos), and [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) functions support 32-bit scroll bar position data, there is a way to circumvent the 16-bit barrier of the [**WM\_HSCROLL**](wm-hscroll.md) and **WM\_VSCROLL** messages.</span></span> <span data-ttu-id="ad400-147">如需技術的說明，請參閱 **GetScrollInfo** 。</span><span class="sxs-lookup"><span data-stu-id="ad400-147">See **GetScrollInfo** for a description of the technique.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad400-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad400-148">Requirements</span></span>



| <span data-ttu-id="ad400-149">需求</span><span class="sxs-lookup"><span data-stu-id="ad400-149">Requirement</span></span> | <span data-ttu-id="ad400-150">值</span><span class="sxs-lookup"><span data-stu-id="ad400-150">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad400-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad400-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ad400-152">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad400-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ad400-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad400-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ad400-154">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad400-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ad400-155">標頭</span><span class="sxs-lookup"><span data-stu-id="ad400-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad400-156"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="ad400-156"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad400-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad400-157">See also</span></span>

<dl> <dt>

<span data-ttu-id="ad400-158">**參考**</span><span class="sxs-lookup"><span data-stu-id="ad400-158">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ad400-159">**GetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="ad400-159">**GetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[<span data-ttu-id="ad400-160">**GetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="ad400-160">**GetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollpos)
</dt> <dt>

[<span data-ttu-id="ad400-161">**GetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="ad400-161">**GetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollrange)
</dt> <dt>

[<span data-ttu-id="ad400-162">**SetScrollInfo**</span><span class="sxs-lookup"><span data-stu-id="ad400-162">**SetScrollInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> <dt>

[<span data-ttu-id="ad400-163">**SetScrollPos**</span><span class="sxs-lookup"><span data-stu-id="ad400-163">**SetScrollPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollpos)
</dt> <dt>

[<span data-ttu-id="ad400-164">**SetScrollRange**</span><span class="sxs-lookup"><span data-stu-id="ad400-164">**SetScrollRange**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setscrollrange)
</dt> <dt>

[<span data-ttu-id="ad400-165">**WM \_ HSCROLL**</span><span class="sxs-lookup"><span data-stu-id="ad400-165">**WM\_HSCROLL**</span></span>](wm-hscroll.md)
</dt> <dt>

[<span data-ttu-id="ad400-166">**WM \_ VSCROLL (的)**</span><span class="sxs-lookup"><span data-stu-id="ad400-166">**WM\_VSCROLL (Trackbar)**</span></span>](wm-vscroll--trackbar-.md)
</dt> </dl>

 

