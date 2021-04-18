---
title: 'WM_RBUTTONUP 訊息 (Winuser .h) '
description: 當使用者放開滑鼠右鍵，而游標位於視窗的工作區時張貼。
ms.assetid: 12d148ba-9324-4db3-b537-b2cd4d0b8f32
keywords:
- WM_RBUTTONUP 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_RBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85a1426b92e8f3aa05c25b551b42ce271b35c673
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968786"
---
# <a name="wm_rbuttonup-message"></a><span data-ttu-id="b588e-104">WM \_ RBUTTONUP 訊息</span><span class="sxs-lookup"><span data-stu-id="b588e-104">WM\_RBUTTONUP message</span></span>

<span data-ttu-id="b588e-105">當使用者放開滑鼠右鍵，而游標位於視窗的工作區時張貼。</span><span class="sxs-lookup"><span data-stu-id="b588e-105">Posted when the user releases the right mouse button while the cursor is in the client area of a window.</span></span> <span data-ttu-id="b588e-106">如果未捕捉到滑鼠，則會將訊息張貼到游標下的視窗。</span><span class="sxs-lookup"><span data-stu-id="b588e-106">If the mouse is not captured, the message is posted to the window beneath the cursor.</span></span> <span data-ttu-id="b588e-107">否則，會將訊息張貼到已捕捉滑鼠的視窗。</span><span class="sxs-lookup"><span data-stu-id="b588e-107">Otherwise, the message is posted to the window that has captured the mouse.</span></span>

<span data-ttu-id="b588e-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="b588e-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_RBUTTONUP                    0x0205
```



## <a name="parameters"></a><span data-ttu-id="b588e-109">參數</span><span class="sxs-lookup"><span data-stu-id="b588e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b588e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b588e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b588e-111">指出不同的虛擬機器碼是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="b588e-111">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="b588e-112">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="b588e-112">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b588e-113">值</span><span class="sxs-lookup"><span data-stu-id="b588e-113">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="b588e-114">意義</span><span class="sxs-lookup"><span data-stu-id="b588e-114">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="b588e-115"><dt>**MK \_控制項**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="b588e-115"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="b588e-116">CTRL 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="b588e-116">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="b588e-117"><dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="b588e-117"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="b588e-118">左邊的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="b588e-118">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="b588e-119"><dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="b588e-119"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="b588e-120">中間的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="b588e-120">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="b588e-121"><dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="b588e-121"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="b588e-122">SHIFT 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="b588e-122">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="b588e-123"><dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="b588e-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="b588e-124">第一個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="b588e-124">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="b588e-125"><dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="b588e-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="b588e-126">第二個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="b588e-126">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="b588e-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b588e-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b588e-128">低序位字組指定游標的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="b588e-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="b588e-129">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="b588e-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="b588e-130">高序位字組指定游標的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="b588e-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="b588e-131">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="b588e-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b588e-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="b588e-132">Return value</span></span>

<span data-ttu-id="b588e-133">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b588e-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b588e-134">備註</span><span class="sxs-lookup"><span data-stu-id="b588e-134">Remarks</span></span>

<span data-ttu-id="b588e-135">使用下列程式碼來取得水準和垂直位置：</span><span class="sxs-lookup"><span data-stu-id="b588e-135">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="b588e-136">如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。</span><span class="sxs-lookup"><span data-stu-id="b588e-136">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="b588e-137">如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="b588e-137">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="b588e-138">您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。</span><span class="sxs-lookup"><span data-stu-id="b588e-138">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b588e-139">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="b588e-139">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="b588e-140">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="b588e-140">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b588e-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="b588e-141">Requirements</span></span>



| <span data-ttu-id="b588e-142">需求</span><span class="sxs-lookup"><span data-stu-id="b588e-142">Requirement</span></span> | <span data-ttu-id="b588e-143">值</span><span class="sxs-lookup"><span data-stu-id="b588e-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b588e-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b588e-144">Minimum supported client</span></span><br/> | <span data-ttu-id="b588e-145">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b588e-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b588e-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b588e-146">Minimum supported server</span></span><br/> | <span data-ttu-id="b588e-147">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b588e-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b588e-148">標頭</span><span class="sxs-lookup"><span data-stu-id="b588e-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="b588e-149"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="b588e-149"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b588e-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b588e-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="b588e-151">**參考**</span><span class="sxs-lookup"><span data-stu-id="b588e-151">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b588e-152">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="b588e-152">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="b588e-153">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="b588e-153">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="b588e-154">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="b588e-154">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="b588e-155">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="b588e-155">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="b588e-156">**WM \_ RBUTTONDBLCLK**</span><span class="sxs-lookup"><span data-stu-id="b588e-156">**WM\_RBUTTONDBLCLK**</span></span>](wm-rbuttondblclk.md)
</dt> <dt>

[<span data-ttu-id="b588e-157">**WM \_ RBUTTONDOWN**</span><span class="sxs-lookup"><span data-stu-id="b588e-157">**WM\_RBUTTONDOWN**</span></span>](wm-rbuttondown.md)
</dt> <dt>

<span data-ttu-id="b588e-158">**概念**</span><span class="sxs-lookup"><span data-stu-id="b588e-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b588e-159">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="b588e-159">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="b588e-160">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="b588e-160">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b588e-161">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="b588e-161">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="b588e-162">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b588e-162">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

