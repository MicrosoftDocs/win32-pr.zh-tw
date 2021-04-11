---
title: 'WM_NCLBUTTONDBLCLK 訊息 (Winuser .h) '
description: 當使用者按兩下滑鼠左鍵，而游標位於視窗的非工作區域內時，即會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。
ms.assetid: fc655631-64d0-4cc5-b85e-25d274182994
keywords:
- WM_NCLBUTTONDBLCLK 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCLBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db66edcb3b1645c6c34c72e35df53afc516dafc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094347"
---
# <a name="wm_nclbuttondblclk-message"></a><span data-ttu-id="eb60b-106">WM \_ NCLBUTTONDBLCLK 訊息</span><span class="sxs-lookup"><span data-stu-id="eb60b-106">WM\_NCLBUTTONDBLCLK message</span></span>

<span data-ttu-id="eb60b-107">當使用者按兩下滑鼠左鍵，而游標位於視窗的非工作區域內時，即會公佈。</span><span class="sxs-lookup"><span data-stu-id="eb60b-107">Posted when the user double-clicks the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="eb60b-108">這則訊息會張貼至包含資料指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="eb60b-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="eb60b-109">如果視窗已捕捉到滑鼠，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="eb60b-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="eb60b-110">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="eb60b-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONDBLCLK              0x00A3
```



## <a name="parameters"></a><span data-ttu-id="eb60b-111">參數</span><span class="sxs-lookup"><span data-stu-id="eb60b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb60b-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb60b-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb60b-113">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式所傳回的點擊測試值，做為處理 [**WM \_ NCHITTEST**](wm-nchittest.md)訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="eb60b-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="eb60b-114">如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。</span><span class="sxs-lookup"><span data-stu-id="eb60b-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="eb60b-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb60b-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb60b-116">[**點**](/previous-versions//dd162808(v=vs.85))結構，包含資料指標的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="eb60b-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="eb60b-117">座標是相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="eb60b-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb60b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="eb60b-118">Return value</span></span>

<span data-ttu-id="eb60b-119">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="eb60b-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb60b-120">備註</span><span class="sxs-lookup"><span data-stu-id="eb60b-120">Remarks</span></span>

<span data-ttu-id="eb60b-121">您也可以使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 和 [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，從 *LPARAM* 中解壓縮 X 和 Y 座標的值。</span><span class="sxs-lookup"><span data-stu-id="eb60b-121">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="eb60b-122">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="eb60b-122">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="eb60b-123">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="eb60b-123">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="eb60b-124">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會測試指定的點以找出資料指標的位置，並執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="eb60b-124">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="eb60b-125">如果有的話， **DefWindowProc** 會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="eb60b-125">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="eb60b-126">視窗不需要 **CS \_ DBLCLKS** 樣式即可接收 **WM \_ NCLBUTTONDBLCLK** 訊息。</span><span class="sxs-lookup"><span data-stu-id="eb60b-126">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCLBUTTONDBLCLK** messages.</span></span>

<span data-ttu-id="eb60b-127">當使用者按下、放開，然後在系統的按兩下時間限制內按下滑鼠左鍵時，系統會產生 **WM \_ NCLBUTTONDBLCLK** 訊息。</span><span class="sxs-lookup"><span data-stu-id="eb60b-127">The system generates a **WM\_NCLBUTTONDBLCLK** message when the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="eb60b-128">按兩下滑鼠左鍵會實際產生四則訊息： [**wm \_ NCLBUTTONDOWN**](wm-nclbuttondown.md)、 [**wm \_ NCLBUTTONUP**](wm-nclbuttonup.md)、 **wm \_ NCLBUTTONDBLCLK** 和 **wm \_ NCLBUTTONUP** 。</span><span class="sxs-lookup"><span data-stu-id="eb60b-128">Double-clicking the left mouse button actually generates four messages: [**WM\_NCLBUTTONDOWN**](wm-nclbuttondown.md), [**WM\_NCLBUTTONUP**](wm-nclbuttonup.md), **WM\_NCLBUTTONDBLCLK**, and **WM\_NCLBUTTONUP** again.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb60b-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb60b-129">Requirements</span></span>



| <span data-ttu-id="eb60b-130">需求</span><span class="sxs-lookup"><span data-stu-id="eb60b-130">Requirement</span></span> | <span data-ttu-id="eb60b-131">值</span><span class="sxs-lookup"><span data-stu-id="eb60b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb60b-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb60b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eb60b-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb60b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="eb60b-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb60b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eb60b-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb60b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eb60b-136">標頭</span><span class="sxs-lookup"><span data-stu-id="eb60b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb60b-137"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="eb60b-137"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb60b-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb60b-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb60b-139">**參考**</span><span class="sxs-lookup"><span data-stu-id="eb60b-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eb60b-140">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="eb60b-140">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="eb60b-141">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="eb60b-141">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="eb60b-142">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="eb60b-142">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="eb60b-143">**WM \_ NCHITTEST**</span><span class="sxs-lookup"><span data-stu-id="eb60b-143">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="eb60b-144">**WM \_ NCLBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="eb60b-144">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="eb60b-145">**WM \_ NCLBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="eb60b-145">**WM\_NCLBUTTONUP**</span></span>](wm-nclbuttonup.md)
</dt> <dt>

[<span data-ttu-id="eb60b-146">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="eb60b-146">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="eb60b-147">**概念**</span><span class="sxs-lookup"><span data-stu-id="eb60b-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="eb60b-148">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="eb60b-148">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="eb60b-149">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="eb60b-149">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="eb60b-150">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="eb60b-150">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="eb60b-151">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb60b-151">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

