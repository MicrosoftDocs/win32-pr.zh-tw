---
title: 'WM_MOUSEHOVER 訊息 (Winuser .h) '
description: 當游標停留在先前呼叫 TrackMouseEvent 所指定的時間期間，將游標停留在視窗的工作區上時，就會張貼至視窗。
ms.assetid: efba7f04-2d26-44f1-89df-a565c03ad944
keywords:
- WM_MOUSEHOVER 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_MOUSEHOVER
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65747ade6bd2ec9456281ac02711de18675a411e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464928"
---
# <a name="wm_mousehover-message"></a><span data-ttu-id="bebfd-104">WM \_ MOUSEHOVER 訊息</span><span class="sxs-lookup"><span data-stu-id="bebfd-104">WM\_MOUSEHOVER message</span></span>

<span data-ttu-id="bebfd-105">當游標停留在先前呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent)所指定的時間期間，將游標停留在視窗的工作區上時，就會張貼至視窗。</span><span class="sxs-lookup"><span data-stu-id="bebfd-105">Posted to a window when the cursor hovers over the client area of the window for the period of time specified in a prior call to [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent).</span></span>

<span data-ttu-id="bebfd-106">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="bebfd-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHOVER                   0x02A1
```



## <a name="parameters"></a><span data-ttu-id="bebfd-107">參數</span><span class="sxs-lookup"><span data-stu-id="bebfd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bebfd-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bebfd-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bebfd-109">指出不同的虛擬機器碼是否已關閉。</span><span class="sxs-lookup"><span data-stu-id="bebfd-109">Indicates whether various virtual keys are down.</span></span> <span data-ttu-id="bebfd-110">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="bebfd-110">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="bebfd-111">值</span><span class="sxs-lookup"><span data-stu-id="bebfd-111">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="bebfd-112">意義</span><span class="sxs-lookup"><span data-stu-id="bebfd-112">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="bebfd-113"><dt>**MK \_控制項**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-113"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="bebfd-114">CTRL 鍵已按下。</span><span class="sxs-lookup"><span data-stu-id="bebfd-114">The CTRL key is depressed.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="bebfd-115"><dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-115"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="bebfd-116">按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="bebfd-116">The left mouse button is depressed.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="bebfd-117"><dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-117"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="bebfd-118">中間的滑鼠按鍵已按下。</span><span class="sxs-lookup"><span data-stu-id="bebfd-118">The middle mouse button is depressed.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="bebfd-119"><dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-119"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="bebfd-120">滑鼠右鍵是按下滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="bebfd-120">The right mouse button is depressed.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="bebfd-121"><dt>**MK \_SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-121"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="bebfd-122">SHIFT 鍵是按下。</span><span class="sxs-lookup"><span data-stu-id="bebfd-122">The SHIFT key is depressed.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="bebfd-123"><dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-123"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="bebfd-124">第一個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="bebfd-124">The first X button is down.</span></span><br/>           |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="bebfd-125"><dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-125"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="bebfd-126">第二個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="bebfd-126">The second X button is down.</span></span><br/>          |



 

</dd> <dt>

<span data-ttu-id="bebfd-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bebfd-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bebfd-128">低序位字組指定游標的 x 座標。</span><span class="sxs-lookup"><span data-stu-id="bebfd-128">The low-order word specifies the x-coordinate of the cursor.</span></span> <span data-ttu-id="bebfd-129">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="bebfd-129">The coordinate is relative to the upper-left corner of the client area.</span></span>

<span data-ttu-id="bebfd-130">高序位字組指定游標的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="bebfd-130">The high-order word specifies the y-coordinate of the cursor.</span></span> <span data-ttu-id="bebfd-131">座標相對於工作區的左上角。</span><span class="sxs-lookup"><span data-stu-id="bebfd-131">The coordinate is relative to the upper-left corner of the client area.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bebfd-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="bebfd-132">Return value</span></span>

<span data-ttu-id="bebfd-133">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="bebfd-133">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="bebfd-134">備註</span><span class="sxs-lookup"><span data-stu-id="bebfd-134">Remarks</span></span>

<span data-ttu-id="bebfd-135">當產生 **WM \_ MOUSEHOVER** 時，會停止停留追蹤。</span><span class="sxs-lookup"><span data-stu-id="bebfd-135">Hover tracking stops when **WM\_MOUSEHOVER** is generated.</span></span> <span data-ttu-id="bebfd-136">如果應用程式需要進一步追蹤滑鼠停留行為，則必須再次呼叫 [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) 。</span><span class="sxs-lookup"><span data-stu-id="bebfd-136">The application must call [**TrackMouseEvent**](/windows/win32/api/winuser/nf-winuser-trackmouseevent) again if it requires further tracking of mouse hover behavior.</span></span>

<span data-ttu-id="bebfd-137">使用下列程式碼來取得水準和垂直位置：</span><span class="sxs-lookup"><span data-stu-id="bebfd-137">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="bebfd-138">如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。</span><span class="sxs-lookup"><span data-stu-id="bebfd-138">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="bebfd-139">如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="bebfd-139">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="bebfd-140">您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。</span><span class="sxs-lookup"><span data-stu-id="bebfd-140">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bebfd-141">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="bebfd-141">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="bebfd-142">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="bebfd-142">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bebfd-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="bebfd-143">Requirements</span></span>



| <span data-ttu-id="bebfd-144">需求</span><span class="sxs-lookup"><span data-stu-id="bebfd-144">Requirement</span></span> | <span data-ttu-id="bebfd-145">值</span><span class="sxs-lookup"><span data-stu-id="bebfd-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bebfd-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bebfd-146">Minimum supported client</span></span><br/> | <span data-ttu-id="bebfd-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bebfd-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bebfd-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bebfd-148">Minimum supported server</span></span><br/> | <span data-ttu-id="bebfd-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bebfd-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bebfd-150">標頭</span><span class="sxs-lookup"><span data-stu-id="bebfd-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="bebfd-151"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="bebfd-151"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bebfd-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bebfd-152">See also</span></span>

<dl> <dt>

<span data-ttu-id="bebfd-153">**參考**</span><span class="sxs-lookup"><span data-stu-id="bebfd-153">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bebfd-154">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="bebfd-154">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="bebfd-155">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="bebfd-155">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="bebfd-156">**GetCapture**</span><span class="sxs-lookup"><span data-stu-id="bebfd-156">**GetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-getcapture)
</dt> <dt>

[<span data-ttu-id="bebfd-157">**SetCapture**</span><span class="sxs-lookup"><span data-stu-id="bebfd-157">**SetCapture**</span></span>](/windows/win32/api/winuser/nf-winuser-setcapture)
</dt> <dt>

[<span data-ttu-id="bebfd-158">**TrackMouseEvent**</span><span class="sxs-lookup"><span data-stu-id="bebfd-158">**TrackMouseEvent**</span></span>](/windows/win32/api/winuser/nf-winuser-trackmouseevent)
</dt> <dt>

[<span data-ttu-id="bebfd-159">**TRACKMOUSEEVENT**</span><span class="sxs-lookup"><span data-stu-id="bebfd-159">**TRACKMOUSEEVENT**</span></span>](/windows/win32/api/winuser/ns-winuser-trackmouseevent)
</dt> <dt>

<span data-ttu-id="bebfd-160">**概念**</span><span class="sxs-lookup"><span data-stu-id="bebfd-160">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bebfd-161">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="bebfd-161">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="bebfd-162">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="bebfd-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bebfd-163">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="bebfd-163">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="bebfd-164">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bebfd-164">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> </dl>

 

