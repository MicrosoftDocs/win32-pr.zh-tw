---
title: 'WM_NCXBUTTONDBLCLK 訊息 (Winuser .h) '
description: 當使用者在滑鼠游標位於視窗的非工作區時，按兩下第一個或第二個 X 按鈕時張貼。 這則訊息會張貼至包含資料指標的視窗。 如果視窗已捕捉到滑鼠，則不會張貼此訊息。
ms.assetid: 8c0b1e96-9cbb-4ef8-83ff-9253f1a934ef
keywords:
- WM_NCXBUTTONDBLCLK 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_NCXBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1455f6d6c2fa40f34bbfbe00e0c7a30daa52f375
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970448"
---
# <a name="wm_ncxbuttondblclk-message"></a><span data-ttu-id="f380f-106">WM \_ NCXBUTTONDBLCLK 訊息</span><span class="sxs-lookup"><span data-stu-id="f380f-106">WM\_NCXBUTTONDBLCLK message</span></span>

<span data-ttu-id="f380f-107">當使用者在滑鼠游標位於視窗的非工作區時，按兩下第一個或第二個 X 按鈕時張貼。</span><span class="sxs-lookup"><span data-stu-id="f380f-107">Posted when the user double-clicks the first or second X button while the cursor is in the nonclient area of a window.</span></span> <span data-ttu-id="f380f-108">這則訊息會張貼至包含資料指標的視窗。</span><span class="sxs-lookup"><span data-stu-id="f380f-108">This message is posted to the window that contains the cursor.</span></span> <span data-ttu-id="f380f-109">如果視窗已捕捉到滑鼠，則不會張貼此訊息。</span><span class="sxs-lookup"><span data-stu-id="f380f-109">If a window has captured the mouse, this message is not posted.</span></span>

<span data-ttu-id="f380f-110">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="f380f-110">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCXBUTTONDBLCLK              0x00AD
```



## <a name="parameters"></a><span data-ttu-id="f380f-111">參數</span><span class="sxs-lookup"><span data-stu-id="f380f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f380f-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f380f-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f380f-113">低序位字組指定 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式所傳回的點擊測試值，使其無法處理 [**WM \_ NCHITTEST**](wm-nchittest.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="f380f-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function from processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="f380f-114">如需點擊測試值的清單，請參閱 **WM \_ NCHITTEST**。</span><span class="sxs-lookup"><span data-stu-id="f380f-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="f380f-115">高序位單字指出按兩下哪一個按鈕。</span><span class="sxs-lookup"><span data-stu-id="f380f-115">The high-order word indicates which button was double-clicked.</span></span> <span data-ttu-id="f380f-116">它可以是下列值之一。</span><span class="sxs-lookup"><span data-stu-id="f380f-116">It can be one of the following values.</span></span>



| <span data-ttu-id="f380f-117">值</span><span class="sxs-lookup"><span data-stu-id="f380f-117">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="f380f-118">意義</span><span class="sxs-lookup"><span data-stu-id="f380f-118">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="f380f-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="f380f-119"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="f380f-120">第一個 X 按鈕按兩下。</span><span class="sxs-lookup"><span data-stu-id="f380f-120">The first X button was double-clicked..</span></span><br/> |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="f380f-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="f380f-121"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="f380f-122">按兩下第二個 X 按鈕。</span><span class="sxs-lookup"><span data-stu-id="f380f-122">The second X button was double-clicked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f380f-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f380f-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f380f-124">[**點**](/previous-versions//dd162808(v=vs.85))結構的指標，其中包含資料指標的 x 和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="f380f-124">A pointer to a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure that contains the x- and y-coordinates of the cursor.</span></span> <span data-ttu-id="f380f-125">座標是相對於畫面的左上角。</span><span class="sxs-lookup"><span data-stu-id="f380f-125">The coordinates are relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f380f-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="f380f-126">Return value</span></span>

<span data-ttu-id="f380f-127">如果應用程式處理此訊息，則應該傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="f380f-127">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="f380f-128">如需處理傳回值的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="f380f-128">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="f380f-129">備註</span><span class="sxs-lookup"><span data-stu-id="f380f-129">Remarks</span></span>

<span data-ttu-id="f380f-130">使用下列程式碼取得 *wParam* 參數中的資訊。</span><span class="sxs-lookup"><span data-stu-id="f380f-130">Use the following code to get the information in the *wParam* parameter.</span></span>


```
nHittest = GET_NCHITTEST_WPARAM(wParam); 
fwButton = GET_XBUTTON_WPARAM(wParam); 
```



<span data-ttu-id="f380f-131">您也可以使用下列程式碼，從 *lParam* 取得 x 和 y 座標：</span><span class="sxs-lookup"><span data-stu-id="f380f-131">You can also use the following code to get the x- and y-coordinates from *lParam*:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



> [!IMPORTANT]
> <span data-ttu-id="f380f-132">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="f380f-132">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="f380f-133">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="f380f-133">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="f380f-134">根據預設， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式會測試指定的點以取得資料指標的位置，並執行適當的動作。</span><span class="sxs-lookup"><span data-stu-id="f380f-134">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function tests the specified point to get the position of the cursor and performs the appropriate action.</span></span> <span data-ttu-id="f380f-135">如果有的話，它會將 [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="f380f-135">If appropriate, it sends the [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the window.</span></span>

<span data-ttu-id="f380f-136">視窗不需要 **CS \_ DBLCLKS** 樣式即可接收 **WM \_ NCXBUTTONDBLCLK** 訊息。</span><span class="sxs-lookup"><span data-stu-id="f380f-136">A window need not have the **CS\_DBLCLKS** style to receive **WM\_NCXBUTTONDBLCLK** messages.</span></span> <span data-ttu-id="f380f-137">當使用者按下、放開，然後再次按下系統的按兩下時間限制內的 X 按鈕時，系統會產生 **WM \_ NCXBUTTONDBLCLK** 訊息。</span><span class="sxs-lookup"><span data-stu-id="f380f-137">The system generates a **WM\_NCXBUTTONDBLCLK** message when the user presses, releases, and again presses an X button within the system's double-click time limit.</span></span> <span data-ttu-id="f380f-138">按兩下其中一個按鈕會實際產生四則訊息： [**wm \_ NCXBUTTONDOWN**](wm-ncxbuttondown.md)、 [**wm \_ NCXBUTTONUP**](wm-ncxbuttonup.md)、 **wm \_ NCXBUTTONDBLCLK** 和 **wm \_ NCXBUTTONUP** 。</span><span class="sxs-lookup"><span data-stu-id="f380f-138">Double-clicking one of these buttons actually generates four messages: [**WM\_NCXBUTTONDOWN**](wm-ncxbuttondown.md), [**WM\_NCXBUTTONUP**](wm-ncxbuttonup.md), **WM\_NCXBUTTONDBLCLK**, and **WM\_NCXBUTTONUP** again.</span></span>

<span data-ttu-id="f380f-139">不同于 [**wm \_ NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md)、 [**wm \_ NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md)和 [**wm \_ NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) 訊息，應用程式應該會在處理時從這個訊息傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="f380f-139">Unlike the [**WM\_NCLBUTTONDBLCLK**](wm-nclbuttondblclk.md), [**WM\_NCMBUTTONDBLCLK**](wm-ncmbuttondblclk.md), and [**WM\_NCRBUTTONDBLCLK**](wm-ncrbuttondblclk.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="f380f-140">這麼做可讓在 Windows 2000 之前的 Windows 系統上模擬此訊息的軟體，判斷視窗程式是否已處理訊息或呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="f380f-140">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="f380f-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="f380f-141">Requirements</span></span>



| <span data-ttu-id="f380f-142">需求</span><span class="sxs-lookup"><span data-stu-id="f380f-142">Requirement</span></span> | <span data-ttu-id="f380f-143">值</span><span class="sxs-lookup"><span data-stu-id="f380f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f380f-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f380f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f380f-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f380f-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f380f-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f380f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f380f-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f380f-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f380f-148">標頭</span><span class="sxs-lookup"><span data-stu-id="f380f-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="f380f-149"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="f380f-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f380f-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f380f-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="f380f-151">**參考**</span><span class="sxs-lookup"><span data-stu-id="f380f-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f380f-152">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f380f-152">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f380f-153">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="f380f-153">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="f380f-154">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="f380f-154">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="f380f-155">**WM \_ NCHITTEST**</span><span class="sxs-lookup"><span data-stu-id="f380f-155">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

[<span data-ttu-id="f380f-156">**WM \_ NCXBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="f380f-156">**WM\_NCXBUTTONDOWN**</span></span>](wm-ncxbuttondown.md)
</dt> <dt>

[<span data-ttu-id="f380f-157">**WM \_ NCXBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="f380f-157">**WM\_NCXBUTTONUP**</span></span>](wm-ncxbuttonup.md)
</dt> <dt>

[<span data-ttu-id="f380f-158">**WM \_ SYSCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="f380f-158">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="f380f-159">**概念**</span><span class="sxs-lookup"><span data-stu-id="f380f-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f380f-160">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="f380f-160">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="f380f-161">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="f380f-161">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f380f-162">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="f380f-162">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="f380f-163">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f380f-163">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

