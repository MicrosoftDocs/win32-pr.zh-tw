---
title: 'WM_NCLBUTTONUP 訊息 (Winuser .h) '
description: 當使用者放開滑鼠左鍵，而游標位於視窗的非工作區域內時，即會公佈。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。
ms.assetid: 0c30dcbd-a4ff-43da-bbd2-fbac1a347c11
keywords:
- WM_NCLBUTTONUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCLBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15df7beefbfa411d00b5a069b68f4ef8cabdff58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024955"
---
# <a name="wm_nclbuttonup-message"></a><span data-ttu-id="38653-106">WM \_ NCLBUTTONUP 訊息</span><span class="sxs-lookup"><span data-stu-id="38653-106">WM\_NCLBUTTONUP message</span></span>

<span data-ttu-id="38653-107">當使用者放開滑鼠左鍵，而游標位於視窗的非工作區域內時，即會公佈。</span><span class="sxs-lookup"><span data-stu-id="38653-107">Posted when the user releases the left mouse button while the cursor is within the nonclient area of a window.</span></span> <span data-ttu-id="38653-108">這則訊息會張貼至包含資料指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="38653-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="38653-109">如果視窗已捕捉到滑鼠，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="38653-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="38653-110">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="38653-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCLBUTTONUP                  0x00A2
```



## <a name="parameters"></a><span data-ttu-id="38653-111">參數</span><span class="sxs-lookup"><span data-stu-id="38653-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38653-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38653-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38653-113">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式所傳回的點擊測試值，做為處理 [**WM \_ NCHITTEST**](wm-nchittest.md)訊息的結果。</span><span class="sxs-lookup"><span data-stu-id="38653-113">The hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="38653-114">如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。</span><span class="sxs-lookup"><span data-stu-id="38653-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

</dd> <dt>

<span data-ttu-id="38653-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38653-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="38653-116">[**點**](/previous-versions//dd162808(v=vs.85))結構，包含資料指標的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="38653-116">A [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="38653-117">座標是相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="38653-117">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38653-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="38653-118">Return value</span></span>

<span data-ttu-id="38653-119">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="38653-119">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="38653-120">備註</span><span class="sxs-lookup"><span data-stu-id="38653-120">Remarks</span></span>

<span data-ttu-id="38653-121">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會測試指定的點，以找出資料指標的位置，並執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="38653-121">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to find out the location of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="38653-122">如果有的話， **DefWindowProc** 會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="38653-122">If appropriate, **DefWindowProc** sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="38653-123">您也可以使用 [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 和 [**get \_ y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏，從 *LPARAM* 中解壓縮 X 和 Y 座標的值。</span><span class="sxs-lookup"><span data-stu-id="38653-123">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to extract the values of the x- and y- coordinates from *lParam*.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="38653-124">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="38653-124">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="38653-125">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="38653-125">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="38653-126">如果適合這麼做，系統會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="38653-126">If it is appropriate to do so, the system sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="38653-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="38653-127">Requirements</span></span>



| <span data-ttu-id="38653-128">需求</span><span class="sxs-lookup"><span data-stu-id="38653-128">Requirement</span></span> | <span data-ttu-id="38653-129">值</span><span class="sxs-lookup"><span data-stu-id="38653-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38653-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38653-130">Minimum supported client</span></span><br/> | <span data-ttu-id="38653-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38653-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="38653-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38653-132">Minimum supported server</span></span><br/> | <span data-ttu-id="38653-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38653-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="38653-134">標頭</span><span class="sxs-lookup"><span data-stu-id="38653-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="38653-135"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="38653-135"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38653-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38653-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="38653-137">**參考**</span><span class="sxs-lookup"><span data-stu-id="38653-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="38653-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="38653-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="38653-139">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="38653-139">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="38653-140">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="38653-140">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="38653-141">**WM \_ NCHITTEST**</span><span class="sxs-lookup"><span data-stu-id="38653-141">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="38653-142">**WM \_ NCLBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="38653-142">**WM\_NCLBUTTONDBLCLK**</span></span>](wm-nclbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="38653-143">**WM \_ NCLBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="38653-143">**WM\_NCLBUTTONDOWN**</span></span>](wm-nclbuttondown.md)
</dt> <dt>

[<span data-ttu-id="38653-144">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="38653-144">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="38653-145">**概念**</span><span class="sxs-lookup"><span data-stu-id="38653-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="38653-146">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="38653-146">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="38653-147">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="38653-147">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="38653-148">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="38653-148">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="38653-149">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="38653-149">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

