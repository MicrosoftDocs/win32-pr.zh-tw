---
title: 'WM_XBUTTONUP 訊息 (Winuser .h) '
description: 當使用者放開第一個或第二個 X 按鈕，而游標位於視窗的工作區時張貼。
ms.assetid: ad726859-368a-4603-bffa-4e639bc69a6a
keywords:
- WM_XBUTTONUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_XBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 08/23/2019
ms.openlocfilehash: 521faefb2e2a76e94a0517c28a5fa812ef34ef5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934748"
---
# <a name="wm_xbuttonup-message"></a><span data-ttu-id="54e9b-104">WM \_ XBUTTONUP 訊息</span><span class="sxs-lookup"><span data-stu-id="54e9b-104">WM\_XBUTTONUP message</span></span>

<span data-ttu-id="54e9b-105">當使用者放開第一個或第二個 X 按鈕，而游標位於視窗的工作區時張貼。</span><span class="sxs-lookup"><span data-stu-id="54e9b-105">Posted when the user releases the first or second X button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="54e9b-106">如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。</span><span class="sxs-lookup"><span data-stu-id="54e9b-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="54e9b-107">否則，會將訊息張貼到已捕捉滑鼠的視窗。</span><span class="sxs-lookup"><span data-stu-id="54e9b-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="54e9b-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="54e9b-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_XBUTTONUP                    0x020C
```



## <a name="parameters"></a><span data-ttu-id="54e9b-109">參數</span><span class="sxs-lookup"><span data-stu-id="54e9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54e9b-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54e9b-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54e9b-111">低序位單字指出是否有不同的虛擬機器碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-111">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="54e9b-112">它可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="54e9b-112">It can be one or more of the following values.</span></span>



| <span data-ttu-id="54e9b-113">值</span><span class="sxs-lookup"><span data-stu-id="54e9b-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="54e9b-114">意義</span><span class="sxs-lookup"><span data-stu-id="54e9b-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="54e9b-115"><dt>**MK \_控制項**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="54e9b-116">CTRL 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="54e9b-117"><dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="54e9b-118">左邊的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="54e9b-119"><dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="54e9b-120">中間的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="54e9b-121"><dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="54e9b-122">滑鼠右鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-122">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="54e9b-123"><dt>**MK \_SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-123"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="54e9b-124">SHIFT 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-124">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="54e9b-125"><dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-125"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="54e9b-126">第一個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-126">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="54e9b-127"><dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-127"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="54e9b-128">第二個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="54e9b-128">The second X button is down.</span></span><br/>     |



 

<span data-ttu-id="54e9b-129">高序位單字表示已發行的按鈕。</span><span class="sxs-lookup"><span data-stu-id="54e9b-129">The high-order word indicates which button was released.</span></span> <span data-ttu-id="54e9b-130">它可能是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="54e9b-130">It can be one of the following values:</span></span>



| <span data-ttu-id="54e9b-131">值</span><span class="sxs-lookup"><span data-stu-id="54e9b-131">Value</span></span>                                                                                                                                                                                                     | <span data-ttu-id="54e9b-132">意義</span><span class="sxs-lookup"><span data-stu-id="54e9b-132">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="XBUTTON1"></span><span id="xbutton1"></span><dl> <span data-ttu-id="54e9b-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-133"><dt>**XBUTTON1**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="54e9b-134">第一個 X 按鈕已釋放。</span><span class="sxs-lookup"><span data-stu-id="54e9b-134">The first X button was released.</span></span><br/>  |
| <span id="XBUTTON2"></span><span id="xbutton2"></span><dl> <span data-ttu-id="54e9b-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-135"><dt>**XBUTTON2**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="54e9b-136">第二個 X 按鈕已釋放。</span><span class="sxs-lookup"><span data-stu-id="54e9b-136">The second X button was released.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="54e9b-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54e9b-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54e9b-138">低序位字組指定游標的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="54e9b-138">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="54e9b-139">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="54e9b-139">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="54e9b-140">高序位字組指定游標的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="54e9b-140">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="54e9b-141">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="54e9b-141">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54e9b-142">傳回值</span><span class="sxs-lookup"><span data-stu-id="54e9b-142">Return value</span></span>

<span data-ttu-id="54e9b-143">如果應用程式處理此訊息，則應該傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="54e9b-143">If an application processes this message, it should return **TRUE**.</span></span> <span data-ttu-id="54e9b-144">如需處理傳回值的詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="54e9b-144">For more information about processing the return value, see the Remarks section.</span></span>

## <a name="remarks"></a><span data-ttu-id="54e9b-145">備註</span><span class="sxs-lookup"><span data-stu-id="54e9b-145">Remarks</span></span>

<span data-ttu-id="54e9b-146">使用下列程式碼來取得 *wParam* 參數中的資訊：</span><span class="sxs-lookup"><span data-stu-id="54e9b-146">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM (wParam); 
fwButton = GET_XBUTTON_WPARAM (wParam); 
```



<span data-ttu-id="54e9b-147">使用下列程式碼來取得水準和垂直位置：</span><span class="sxs-lookup"><span data-stu-id="54e9b-147">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="54e9b-148">如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。</span><span class="sxs-lookup"><span data-stu-id="54e9b-148">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="54e9b-149">如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="54e9b-149">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="54e9b-150">您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。</span><span class="sxs-lookup"><span data-stu-id="54e9b-150">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="54e9b-151">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="54e9b-151">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="54e9b-152">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="54e9b-152">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="54e9b-153">不同于 [**wm \_ LBUTTONUP**](wm-lbuttonup.md)、 [**wm \_ MBUTTONUP**](wm-mbuttonup.md)和 [**wm \_ RBUTTONUP**](wm-rbuttonup.md) 訊息，應用程式應該會在處理時從這個訊息傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="54e9b-153">Unlike the [**WM\_LBUTTONUP**](wm-lbuttonup.md), [**WM\_MBUTTONUP**](wm-mbuttonup.md), and [**WM\_RBUTTONUP**](wm-rbuttonup.md) messages, an application should return **TRUE** from this message if it processes it.</span></span> <span data-ttu-id="54e9b-154">這麼做可讓在 Windows 2000 之前的 Windows 系統上模擬此訊息的軟體，判斷視窗程式是否已處理訊息或呼叫 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 來處理訊息。</span><span class="sxs-lookup"><span data-stu-id="54e9b-154">Doing so will allow software that simulates this message on Windows systems earlier than Windows 2000 to determine whether the window procedure processed the message or called [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) to process it.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e9b-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="54e9b-155">Requirements</span></span>



| <span data-ttu-id="54e9b-156">需求</span><span class="sxs-lookup"><span data-stu-id="54e9b-156">Requirement</span></span> | <span data-ttu-id="54e9b-157">值</span><span class="sxs-lookup"><span data-stu-id="54e9b-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e9b-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54e9b-158">Minimum supported client</span></span><br/> | <span data-ttu-id="54e9b-159">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54e9b-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="54e9b-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54e9b-160">Minimum supported server</span></span><br/> | <span data-ttu-id="54e9b-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="54e9b-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="54e9b-162">標頭</span><span class="sxs-lookup"><span data-stu-id="54e9b-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="54e9b-163"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="54e9b-163"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e9b-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54e9b-164">See also</span></span>

<dl> <dt>

<span data-ttu-id="54e9b-165">**參考**</span><span class="sxs-lookup"><span data-stu-id="54e9b-165">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="54e9b-166">**取得 \_ KEYSTATE \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="54e9b-166">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="54e9b-167">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="54e9b-167">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="54e9b-168">**取得 \_ XBUTTON \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="54e9b-168">**GET\_XBUTTON\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_xbutton_wparam)
</dt> <dt>

[<span data-ttu-id="54e9b-169">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="54e9b-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="54e9b-170">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="54e9b-170">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="54e9b-171">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="54e9b-171">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="54e9b-172">**WM \_ XBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="54e9b-172">**WM\_XBUTTONDBLCLK**</span></span>](wm-xbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="54e9b-173">**WM \_ XBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="54e9b-173">**WM\_XBUTTONDOWN**</span></span>](wm-xbuttondown.md)
</dt> <dt>

<span data-ttu-id="54e9b-174">**概念**</span><span class="sxs-lookup"><span data-stu-id="54e9b-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54e9b-175">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="54e9b-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="54e9b-176">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="54e9b-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="54e9b-177">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="54e9b-177">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="54e9b-178">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54e9b-178">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

