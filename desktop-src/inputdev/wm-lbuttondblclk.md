---
title: 'WM_LBUTTONDBLCLK 訊息 (Winuser .h) '
description: 當使用者按兩下滑鼠左鍵，而游標位於視窗的工作區時，則會公佈。
ms.assetid: 370aa19e-4939-4ac3-9c0b-137a9792e52a
keywords:
- WM_LBUTTONDBLCLK 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_LBUTTONDBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fd91eef026ae027e183b4f304211915e7bbbd95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965079"
---
# <a name="wm_lbuttondblclk-message"></a><span data-ttu-id="80c22-104">WM \_ LBUTTONDBLCLK 訊息</span><span class="sxs-lookup"><span data-stu-id="80c22-104">WM\_LBUTTONDBLCLK message</span></span>

<span data-ttu-id="80c22-105">當使用者按兩下滑鼠左鍵，而游標位於視窗的工作區時，則會公佈。</span><span class="sxs-lookup"><span data-stu-id="80c22-105">Posted when the user double-clicks the left mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="80c22-106">如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。</span><span class="sxs-lookup"><span data-stu-id="80c22-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="80c22-107">否則，會將訊息張貼到已捕捉滑鼠的視窗。</span><span class="sxs-lookup"><span data-stu-id="80c22-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="80c22-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="80c22-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_LBUTTONDBLCLK                0x0203
```



## <a name="parameters"></a><span data-ttu-id="80c22-109">參數</span><span class="sxs-lookup"><span data-stu-id="80c22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c22-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80c22-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80c22-111">指出不同的虛擬機器碼是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="80c22-112">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="80c22-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="80c22-113">值</span><span class="sxs-lookup"><span data-stu-id="80c22-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="80c22-114">意義</span><span class="sxs-lookup"><span data-stu-id="80c22-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="80c22-115"><dt>**MK \_控制項**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="80c22-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="80c22-116">CTRL 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="80c22-117"><dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="80c22-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="80c22-118">左邊的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="80c22-119"><dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="80c22-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="80c22-120">中間的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="80c22-121"><dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="80c22-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="80c22-122">滑鼠右鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="80c22-123"><dt>**MK \_SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="80c22-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="80c22-124">SHIFT 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="80c22-125"><dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="80c22-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="80c22-126">第一個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="80c22-127"><dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="80c22-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="80c22-128">第二個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="80c22-128">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="80c22-129">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80c22-129">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80c22-130">低序位字組指定游標的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="80c22-130">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="80c22-131">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="80c22-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="80c22-132">高序位字組指定游標的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="80c22-132">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="80c22-133">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="80c22-133">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c22-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="80c22-134">Return value</span></span>

<span data-ttu-id="80c22-135">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="80c22-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="80c22-136">備註</span><span class="sxs-lookup"><span data-stu-id="80c22-136">Remarks</span></span>

<span data-ttu-id="80c22-137">使用下列程式碼來取得水準和垂直位置：</span><span class="sxs-lookup"><span data-stu-id="80c22-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="80c22-138">如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。</span><span class="sxs-lookup"><span data-stu-id="80c22-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="80c22-139">如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="80c22-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="80c22-140">您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。</span><span class="sxs-lookup"><span data-stu-id="80c22-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80c22-141">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="80c22-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="80c22-142">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="80c22-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="80c22-143">只有具有 **CS \_ DBLCLKS** 樣式的視窗可以接收 **WM \_ LBUTTONDBLCLK** 訊息，每次使用者按下、放開，然後在系統的按兩下時間限制內按下滑鼠左鍵時，系統就會產生此訊息。</span><span class="sxs-lookup"><span data-stu-id="80c22-143">Only windows that have the **CS\_DBLCLKS** style can receive **WM\_LBUTTONDBLCLK** messages, which the system generates whenever the user presses, releases, and again presses the left mouse button within the system's double-click time limit.</span></span> <span data-ttu-id="80c22-144">按兩下滑鼠左鍵會實際產生四個訊息的一連串： [**wm \_ LBUTTONDOWN**](wm-lbuttondown.md)、 [**wm \_ LBUTTONUP**](wm-lbuttonup.md)、 **wm \_ LBUTTONDBLCLK** 和 **wm \_ LBUTTONUP**。</span><span class="sxs-lookup"><span data-stu-id="80c22-144">Double-clicking the left mouse button actually generates a sequence of four messages: [**WM\_LBUTTONDOWN**](wm-lbuttondown.md), [**WM\_LBUTTONUP**](wm-lbuttonup.md), **WM\_LBUTTONDBLCLK**, and **WM\_LBUTTONUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="80c22-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="80c22-145">Requirements</span></span>



| <span data-ttu-id="80c22-146">需求</span><span class="sxs-lookup"><span data-stu-id="80c22-146">Requirement</span></span> | <span data-ttu-id="80c22-147">值</span><span class="sxs-lookup"><span data-stu-id="80c22-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80c22-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80c22-148">Minimum supported client</span></span><br/> | <span data-ttu-id="80c22-149">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80c22-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80c22-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80c22-150">Minimum supported server</span></span><br/> | <span data-ttu-id="80c22-151">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80c22-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="80c22-152">標頭</span><span class="sxs-lookup"><span data-stu-id="80c22-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="80c22-153"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="80c22-153"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80c22-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80c22-154">See also</span></span>

<dl> <dt>

<span data-ttu-id="80c22-155">**參考**</span><span class="sxs-lookup"><span data-stu-id="80c22-155">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="80c22-156">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="80c22-156">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="80c22-157">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="80c22-157">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="80c22-158">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="80c22-158">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="80c22-159">**GetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="80c22-159">**GetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-getdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="80c22-160">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="80c22-160">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="80c22-161">**SetDoubleClickTime**</span><span class="sxs-lookup"><span data-stu-id="80c22-161">**SetDoubleClickTime**</span></span>](/windows/win32/api/winuser/nf-winuser-setdoubleclicktime)
</dt> <dt>

[<span data-ttu-id="80c22-162">**WM \_ LBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="80c22-162">**WM\_LBUTTONDOWN**</span></span>](wm-lbuttondown.md)
</dt> <dt>

[<span data-ttu-id="80c22-163">**WM \_ LBUTTONUP**</span><span class="sxs-lookup"><span data-stu-id="80c22-163">**WM\_LBUTTONUP**</span></span>](wm-lbuttonup.md)
</dt> <dt>

<span data-ttu-id="80c22-164">**概念**</span><span class="sxs-lookup"><span data-stu-id="80c22-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="80c22-165">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="80c22-165">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="80c22-166">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="80c22-166">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="80c22-167">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="80c22-167">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="80c22-168">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="80c22-168">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

