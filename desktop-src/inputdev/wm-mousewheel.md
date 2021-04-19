---
title: 'WM_MOUSEWHEEL 訊息 (Winuser .h) '
description: 當滑鼠滾輪旋轉時，傳送至焦點視窗。
ms.assetid: 9831cceb-bbf3-42a0-a0f9-c2d6ad4573eb
keywords:
- WM_MOUSEWHEEL 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_MOUSEWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b918989b41b43c3f54d8ec3133223716e839e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966920"
---
# <a name="wm_mousewheel-message"></a><span data-ttu-id="13a99-104">WM \_ 滑鼠滾輪訊息</span><span class="sxs-lookup"><span data-stu-id="13a99-104">WM\_MOUSEWHEEL message</span></span>

<span data-ttu-id="13a99-105">當滑鼠滾輪旋轉時，傳送至焦點視窗。</span><span class="sxs-lookup"><span data-stu-id="13a99-105">Sent to the focus window when the mouse wheel is rotated.</span></span> <span data-ttu-id="13a99-106">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將訊息傳播至視窗的父代。</span><span class="sxs-lookup"><span data-stu-id="13a99-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="13a99-107">訊息不應該有內部轉送，因為 **DefWindowProc** 會將它傳播到父鏈上，直到它找到處理它的視窗為止。</span><span class="sxs-lookup"><span data-stu-id="13a99-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="13a99-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="13a99-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEWHEEL                   0x020A
```



## <a name="parameters"></a><span data-ttu-id="13a99-109">參數</span><span class="sxs-lookup"><span data-stu-id="13a99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a99-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13a99-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13a99-111">高序位單字表示滾輪旋轉的距離，以 **滾輪 \_ DELTA** 的倍數或間隔表示，也就是120。</span><span class="sxs-lookup"><span data-stu-id="13a99-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or divisions of **WHEEL\_DELTA**, which is 120.</span></span> <span data-ttu-id="13a99-112">正值表示滾輪向前旋轉，離開使用者;負數值表示滾輪朝使用者向後旋轉。</span><span class="sxs-lookup"><span data-stu-id="13a99-112">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span>

<span data-ttu-id="13a99-113">低序位單字指出是否有不同的虛擬機器碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="13a99-114">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="13a99-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="13a99-115">值</span><span class="sxs-lookup"><span data-stu-id="13a99-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="13a99-116">意義</span><span class="sxs-lookup"><span data-stu-id="13a99-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="13a99-117"><dt>**MK \_控制項**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="13a99-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="13a99-118">CTRL 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="13a99-119"><dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="13a99-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="13a99-120">左邊的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="13a99-121"><dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="13a99-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="13a99-122">中間的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="13a99-123"><dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="13a99-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="13a99-124">滑鼠右鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="13a99-125"><dt>**MK \_SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="13a99-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="13a99-126">SHIFT 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="13a99-127"><dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="13a99-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="13a99-128">第一個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="13a99-129"><dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="13a99-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="13a99-130">第二個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="13a99-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="13a99-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13a99-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13a99-132">低序位字指定指標的 x 座標（相對於畫面的左上角）。</span><span class="sxs-lookup"><span data-stu-id="13a99-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="13a99-133">高序位字指定指標的 y 座標（相對於畫面的左上角）。</span><span class="sxs-lookup"><span data-stu-id="13a99-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a99-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="13a99-134">Return value</span></span>

<span data-ttu-id="13a99-135">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="13a99-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13a99-136">備註</span><span class="sxs-lookup"><span data-stu-id="13a99-136">Remarks</span></span>

<span data-ttu-id="13a99-137">使用下列程式碼來取得 *wParam* 參數中的資訊：</span><span class="sxs-lookup"><span data-stu-id="13a99-137">Use the following code to get the information in the *wParam* parameter:</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="13a99-138">使用下列程式碼來取得水準和垂直位置：</span><span class="sxs-lookup"><span data-stu-id="13a99-138">Use the following code to obtain the horizontal and vertical position:</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



<span data-ttu-id="13a99-139">如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。</span><span class="sxs-lookup"><span data-stu-id="13a99-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="13a99-140">如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="13a99-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="13a99-141">您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。</span><span class="sxs-lookup"><span data-stu-id="13a99-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="13a99-142">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="13a99-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="13a99-143">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="13a99-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="13a99-144">滾輪旋轉將會是在120設定的 **滾輪 \_ 差異** 的倍數。</span><span class="sxs-lookup"><span data-stu-id="13a99-144">The wheel rotation will be a multiple of **WHEEL\_DELTA**, which is set at 120.</span></span> <span data-ttu-id="13a99-145">這是所要採取動作的臨界值，而其中一個這類動作 (例如，每個差異都應進行滾動一個遞增) 。</span><span class="sxs-lookup"><span data-stu-id="13a99-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="13a99-146">差異設定為120，可讓 Microsoft 或其他廠商建立更精細的解析度滾輪， (無凹槽) 的自由旋轉滾輪，以每次旋轉傳送更多訊息，但每個訊息中的值較小。</span><span class="sxs-lookup"><span data-stu-id="13a99-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="13a99-147">若要使用此功能，您可以新增傳入的 delta 值，直到達到 **輪子 \_ delta** 為止 (因此，若要進行差異輪替，您會收到相同的回應) ，或滾動部分行以回應較頻繁的訊息。</span><span class="sxs-lookup"><span data-stu-id="13a99-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to the more frequent messages.</span></span> <span data-ttu-id="13a99-148">您也可以選擇您的捲軸細微性，並累計差異直到到達為止。</span><span class="sxs-lookup"><span data-stu-id="13a99-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

<span data-ttu-id="13a99-149">請注意， **MSH \_ 滑鼠滾輪** 沒有任何 *fwKeys* 。</span><span class="sxs-lookup"><span data-stu-id="13a99-149">Note, there is no *fwKeys* for **MSH\_MOUSEWHEEL**.</span></span> <span data-ttu-id="13a99-150">否則，這些參數與適用于 **WM \_ 滑鼠滾輪** 的參數完全相同。</span><span class="sxs-lookup"><span data-stu-id="13a99-150">Otherwise, the parameters are exactly the same as for **WM\_MOUSEWHEEL**.</span></span>

<span data-ttu-id="13a99-151">應用程式是由應用程式將 **MSH \_ 滑鼠滾輪** 轉送到任何内嵌物件或控制項。</span><span class="sxs-lookup"><span data-stu-id="13a99-151">It is up to the application to forward **MSH\_MOUSEWHEEL** to any embedded objects or controls.</span></span> <span data-ttu-id="13a99-152">需要應用程式才能將訊息傳送至使用中的內嵌 OLE 應用程式。</span><span class="sxs-lookup"><span data-stu-id="13a99-152">The application is required to send the message to an active embedded OLE application.</span></span> <span data-ttu-id="13a99-153">應用程式會將其傳送至具有焦點的啟用滾輪控制項，這是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="13a99-153">It is optional that the application sends it to a wheel-enabled control with focus.</span></span> <span data-ttu-id="13a99-154">如果應用程式將訊息傳送至控制項，則可以檢查傳回值，以查看是否已處理訊息。</span><span class="sxs-lookup"><span data-stu-id="13a99-154">If the application does send the message to a control, it can check the return value to see if the message was processed.</span></span> <span data-ttu-id="13a99-155">如果控制項處理訊息，則必須傳回 **TRUE** 值。</span><span class="sxs-lookup"><span data-stu-id="13a99-155">Controls are required to return a value of **TRUE** if they process the message.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a99-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="13a99-156">Requirements</span></span>



| <span data-ttu-id="13a99-157">需求</span><span class="sxs-lookup"><span data-stu-id="13a99-157">Requirement</span></span> | <span data-ttu-id="13a99-158">值</span><span class="sxs-lookup"><span data-stu-id="13a99-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13a99-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13a99-159">Minimum supported client</span></span><br/> | <span data-ttu-id="13a99-160">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a99-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="13a99-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13a99-161">Minimum supported server</span></span><br/> | <span data-ttu-id="13a99-162">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a99-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="13a99-163">標頭</span><span class="sxs-lookup"><span data-stu-id="13a99-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="13a99-164"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="13a99-164"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a99-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13a99-165">See also</span></span>

<dl> <dt>

<span data-ttu-id="13a99-166">**參考**</span><span class="sxs-lookup"><span data-stu-id="13a99-166">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="13a99-167">**取得 \_ KEYSTATE \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="13a99-167">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="13a99-168">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="13a99-168">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="13a99-169">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="13a99-169">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="13a99-170">**取得 \_ 輪子 \_ DELTA \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="13a99-170">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="13a99-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="13a99-171">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="13a99-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="13a99-172">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="13a99-173">**滑鼠 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="13a99-173">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="13a99-174">**概念**</span><span class="sxs-lookup"><span data-stu-id="13a99-174">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="13a99-175">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="13a99-175">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="13a99-176">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="13a99-176">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="13a99-177">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="13a99-177">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="13a99-178">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="13a99-178">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="13a99-179">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="13a99-179">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="13a99-180">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="13a99-180">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

