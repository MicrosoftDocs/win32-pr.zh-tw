---
title: 'WM_NCMBUTTONUP 訊息 (Winuser .h) '
description: 當使用者放開滑鼠左鍵，而游標位於視窗的非工作區時，則會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。
ms.assetid: 93335e46-c72b-4139-9785-67ce2a6bcb4a
keywords:
- WM_NCMBUTTONUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCMBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a890c79f6835dc0f44257fc1adf5d00b976a87c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969775"
---
# <a name="wm_ncmbuttonup-message"></a><span data-ttu-id="1452b-106">WM \_ NCMBUTTONUP 訊息</span><span class="sxs-lookup"><span data-stu-id="1452b-106">WM\_NCMBUTTONUP message</span></span>

<span data-ttu-id="1452b-107">當使用者放開滑鼠左鍵，而游標位於視窗的非工作區時，則會公佈。</span><span class="sxs-lookup"><span data-stu-id="1452b-107">Posted when the user releases the middle mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="1452b-108">這則訊息會張貼至包含資料指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="1452b-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="1452b-109">如果視窗已捕捉到滑鼠，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="1452b-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="1452b-110">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="1452b-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCMBUTTONUP                  0x00A8
```



## <a name="parameters"></a><span data-ttu-id="1452b-111">參數</span><span class="sxs-lookup"><span data-stu-id="1452b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1452b-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1452b-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1452b-113">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式所傳回的點擊測試值，做為處理 [**WM \_ NCHITTEST**](wm-nchittest.md)訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="1452b-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="1452b-114">如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。</span><span class="sxs-lookup"><span data-stu-id="1452b-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="1452b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1452b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1452b-116">[**點**](/previous-versions//dd162808(v=vs.85))結構，包含資料指標的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="1452b-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="1452b-117">座標是相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="1452b-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1452b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="1452b-118">Return value</span></span>

<span data-ttu-id="1452b-119">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1452b-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1452b-120">備註</span><span class="sxs-lookup"><span data-stu-id="1452b-120">Remarks</span></span>

<span data-ttu-id="1452b-121">您也可以使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 和 [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，從 *LPARAM* 中解壓縮 X 和 Y 座標的值。</span><span class="sxs-lookup"><span data-stu-id="1452b-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="1452b-122">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="1452b-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="1452b-123">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="1452b-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="1452b-124">如果適合這麼做，系統會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="1452b-124">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="1452b-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="1452b-125">Requirements</span></span>



| <span data-ttu-id="1452b-126">需求</span><span class="sxs-lookup"><span data-stu-id="1452b-126">Requirement</span></span> | <span data-ttu-id="1452b-127">值</span><span class="sxs-lookup"><span data-stu-id="1452b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1452b-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1452b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1452b-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1452b-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1452b-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1452b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1452b-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1452b-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1452b-132">標頭</span><span class="sxs-lookup"><span data-stu-id="1452b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1452b-133"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="1452b-133"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1452b-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1452b-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="1452b-135">**參考**</span><span class="sxs-lookup"><span data-stu-id="1452b-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1452b-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1452b-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1452b-137">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="1452b-137">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="1452b-138">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="1452b-138">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="1452b-139">**WM \_ NCHITTEST**</span><span class="sxs-lookup"><span data-stu-id="1452b-139">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="1452b-140">**WM \_ NCMBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="1452b-140">**WM\_NCMBUTTONDBLCLK**</span></span>](wm-ncmbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="1452b-141">**WM \_ NCMBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="1452b-141">**WM\_NCMBUTTONDOWN**</span></span>](wm-ncmbuttondown.md)
</dt> <dt>

[<span data-ttu-id="1452b-142">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="1452b-142">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="1452b-143">**概念**</span><span class="sxs-lookup"><span data-stu-id="1452b-143">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1452b-144">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="1452b-144">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="1452b-145">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="1452b-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="1452b-146">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="1452b-146">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="1452b-147">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1452b-147">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

