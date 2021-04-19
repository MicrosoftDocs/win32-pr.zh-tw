---
title: 'WM_MOUSEHWHEEL 訊息 (Winuser .h) '
description: 當滑鼠的水準滾輪傾斜或旋轉時，傳送至使用中視窗。
ms.assetid: 4d6a3d73-38ef-450d-89d2-2d381fc7a7c3
keywords:
- WM_MOUSEHWHEEL 訊息鍵盤和滑鼠輸入
topic_type:
- apiref
api_name:
- WM_MOUSEHWHEEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c1f3b1690ad39919e2a62b50ba6eacec8348e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967963"
---
# <a name="wm_mousehwheel-message"></a><span data-ttu-id="a4b5d-104">WM \_ MOUSEHWHEEL 訊息</span><span class="sxs-lookup"><span data-stu-id="a4b5d-104">WM\_MOUSEHWHEEL message</span></span>

<span data-ttu-id="a4b5d-105">當滑鼠的水準滾輪傾斜或旋轉時，傳送至使用中視窗。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-105">Sent to the active window when the mouse's horizontal scroll wheel is tilted or rotated.</span></span> <span data-ttu-id="a4b5d-106">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會將訊息傳播至視窗的父代。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-106">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function propagates the message to the window's parent.</span></span> <span data-ttu-id="a4b5d-107">訊息不應該有內部轉送，因為 **DefWindowProc** 會將它傳播到父鏈上，直到它找到處理它的視窗為止。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-107">There should be no internal forwarding of the message, since **DefWindowProc** propagates it up the parent chain until it finds a window that processes it.</span></span>

<span data-ttu-id="a4b5d-108">視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEHWHEEL                  0x020E
```



## <a name="parameters"></a><span data-ttu-id="a4b5d-109">參數</span><span class="sxs-lookup"><span data-stu-id="a4b5d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4b5d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a4b5d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4b5d-111">高序位單字表示滾輪旋轉的距離，以重數或 **輪子 \_ DELTA** 的因數表示，其設定為120。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-111">The high-order word indicates the distance the wheel is rotated, expressed in multiples or factors of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="a4b5d-112">正值表示滾輪已向右旋轉;負數值表示滾輪已向左旋轉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-112">A positive value indicates that the wheel was rotated to the right; a negative value indicates that the wheel was rotated to the left.</span></span>

<span data-ttu-id="a4b5d-113">低序位單字指出是否有不同的虛擬機器碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-113">The low-order word indicates whether various virtual keys are down.</span></span> <span data-ttu-id="a4b5d-114">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-114">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="a4b5d-115">值</span><span class="sxs-lookup"><span data-stu-id="a4b5d-115">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="a4b5d-116">意義</span><span class="sxs-lookup"><span data-stu-id="a4b5d-116">Meaning</span></span>                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="MK_CONTROL"></span><span id="mk_control"></span><dl> <span data-ttu-id="a4b5d-117"><dt>**MK \_控制項**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-117"><dt>**MK\_CONTROL**</dt> <dt>0x0008</dt></span></span> </dl>    | <span data-ttu-id="a4b5d-118">CTRL 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-118">The CTRL key is down.</span></span><br/>            |
| <span id="MK_LBUTTON"></span><span id="mk_lbutton"></span><dl> <span data-ttu-id="a4b5d-119"><dt>**MK \_LBUTTON**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-119"><dt>**MK\_LBUTTON**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="a4b5d-120">左邊的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-120">The left mouse button is down.</span></span><br/>   |
| <span id="MK_MBUTTON"></span><span id="mk_mbutton"></span><dl> <span data-ttu-id="a4b5d-121"><dt>**MK \_MBUTTON**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-121"><dt>**MK\_MBUTTON**</dt> <dt>0x0010</dt></span></span> </dl>    | <span data-ttu-id="a4b5d-122">中間的滑鼠按鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-122">The middle mouse button is down.</span></span><br/> |
| <span id="MK_RBUTTON"></span><span id="mk_rbutton"></span><dl> <span data-ttu-id="a4b5d-123"><dt>**MK \_RBUTTON**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-123"><dt>**MK\_RBUTTON**</dt> <dt>0x0002</dt></span></span> </dl>    | <span data-ttu-id="a4b5d-124">滑鼠右鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-124">The right mouse button is down.</span></span><br/>  |
| <span id="MK_SHIFT"></span><span id="mk_shift"></span><dl> <span data-ttu-id="a4b5d-125"><dt>**MK \_SHIFT**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-125"><dt>**MK\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>          | <span data-ttu-id="a4b5d-126">SHIFT 鍵已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-126">The SHIFT key is down.</span></span><br/>           |
| <span id="MK_XBUTTON1"></span><span id="mk_xbutton1"></span><dl> <span data-ttu-id="a4b5d-127"><dt>**MK \_XBUTTON1**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-127"><dt>**MK\_XBUTTON1**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="a4b5d-128">第一個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-128">The first X button is down.</span></span><br/>      |
| <span id="MK_XBUTTON2"></span><span id="mk_xbutton2"></span><dl> <span data-ttu-id="a4b5d-129"><dt>**MK \_XBUTTON2**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-129"><dt>**MK\_XBUTTON2**</dt> <dt>0x0040</dt></span></span> </dl> | <span data-ttu-id="a4b5d-130">第二個 X 按鈕已關閉。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-130">The second X button is down.</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="a4b5d-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a4b5d-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a4b5d-132">低序位字指定指標的 x 座標（相對於畫面的左上角）。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-132">The low-order word specifies the x-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

<span data-ttu-id="a4b5d-133">高序位字指定指標的 y 座標（相對於畫面的左上角）。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-133">The high-order word specifies the y-coordinate of the pointer, relative to the upper-left corner of the screen.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4b5d-134">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4b5d-134">Return value</span></span>

<span data-ttu-id="a4b5d-135">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-135">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b5d-136">備註</span><span class="sxs-lookup"><span data-stu-id="a4b5d-136">Remarks</span></span>

<span data-ttu-id="a4b5d-137">使用下列程式碼來取得 *wParam* 參數中的資訊。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-137">Use the following code to obtain the information in the *wParam* parameter.</span></span>


```
fwKeys = GET_KEYSTATE_WPARAM(wParam);
zDelta = GET_WHEEL_DELTA_WPARAM(wParam);
```



<span data-ttu-id="a4b5d-138">使用下列程式碼來取得水準和垂直位置。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-138">Use the following code to obtain the horizontal and vertical position.</span></span>


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="a4b5d-139">如上面所述，x 座標是在傳回值的低序位 **短** 時間內;y 座標是在高序位的 **短** (兩者都代表 *帶* 正負號的值，因為它們可以在具有多個監視器) 的系統上採用負數值。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-139">As noted above, the x-coordinate is in the low-order **short** of the return value; the y-coordinate is in the high-order **short** (both represent *signed* values because they can take negative values on systems with multiple monitors).</span></span> <span data-ttu-id="a4b5d-140">如果將傳回值指派給變數，您可以使用 [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) 宏從傳回值取得 [**點**](/previous-versions//dd162808(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-140">If the return value is assigned to a variable, you can use the [**MAKEPOINTS**](/windows/desktop/api/wingdi/nf-wingdi-makepoints) macro to obtain a [**POINTS**](/previous-versions//dd162808(v=vs.85)) structure from the return value.</span></span> <span data-ttu-id="a4b5d-141">您也可以使用 [**get \_ x \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) 或 [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) 宏來解壓縮 X 或 y 座標。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-141">You can also use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) or [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macro to extract the x- or y-coordinate.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4b5d-142">請勿使用 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 或 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) 宏來將游標位置的 x 和 y 座標解壓縮，因為這些宏會在具有多個監視器的系統上傳回不正確的結果。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-142">Do not use the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) or [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros to extract the x- and y- coordinates of the cursor position because these macros return incorrect results on systems with multiple monitors.</span></span> <span data-ttu-id="a4b5d-143">具有多個監視器的系統可以有負值的 x 和 y 座標，而 **LOWORD** 和 **HIWORD** 會將座標視為不帶正負號的數量。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-143">Systems with multiple monitors can have negative x- and y- coordinates, and **LOWORD** and **HIWORD** treat the coordinates as unsigned quantities.</span></span>

 

<span data-ttu-id="a4b5d-144">滾輪旋轉是 **滾輪 \_ 差異** 的倍數，其設定為120。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-144">The wheel rotation is a multiple of **WHEEL\_DELTA**, which is set to 120.</span></span> <span data-ttu-id="a4b5d-145">這是所要採取動作的臨界值，而其中一個這類動作 (例如，每個差異都應進行滾動一個遞增) 。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-145">This is the threshold for action to be taken, and one such action (for example, scrolling one increment) should occur for each delta.</span></span>

<span data-ttu-id="a4b5d-146">差異已設定為120，可讓 Microsoft 或其他廠商建立更精細的解析度滾輪 (例如，無凹槽的自由旋轉滾輪) 在每次旋轉時傳送更多訊息，但每則訊息中的值較小。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-146">The delta was set to 120 to allow Microsoft or other vendors to build finer-resolution wheels (for example, a freely-rotating wheel with no notches) to send more messages per rotation, but with a smaller value in each message.</span></span> <span data-ttu-id="a4b5d-147">若要使用此功能，您可以新增傳入的 delta 值，直到達到 **輪子 \_ delta** 為止 (因此，若為差異旋轉，您會收到相同的回應) ，或滾動部分行以回應更頻繁的訊息。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-147">To use this feature, you can either add the incoming delta values until **WHEEL\_DELTA** is reached (so for a delta-rotation you get the same response), or scroll partial lines in response to more frequent messages.</span></span> <span data-ttu-id="a4b5d-148">您也可以選擇您的捲軸細微性，並累計差異直到到達為止。</span><span class="sxs-lookup"><span data-stu-id="a4b5d-148">You can also choose your scroll granularity and accumulate deltas until it is reached.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b5d-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4b5d-149">Requirements</span></span>



| <span data-ttu-id="a4b5d-150">需求</span><span class="sxs-lookup"><span data-stu-id="a4b5d-150">Requirement</span></span> | <span data-ttu-id="a4b5d-151">值</span><span class="sxs-lookup"><span data-stu-id="a4b5d-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b5d-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4b5d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b5d-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b5d-153">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="a4b5d-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4b5d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b5d-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b5d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a4b5d-156">標頭</span><span class="sxs-lookup"><span data-stu-id="a4b5d-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b5d-157"><dt>Winuser (包含 Windowsx) </dt></span><span class="sxs-lookup"><span data-stu-id="a4b5d-157"><dt>Winuser.h (include Windowsx.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b5d-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4b5d-158">See also</span></span>

<dl> <dt>

<span data-ttu-id="a4b5d-159">**參考**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-159">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a4b5d-160">**取得 \_ KEYSTATE \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-160">**GET\_KEYSTATE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_keystate_wparam)
</dt> <dt>

[<span data-ttu-id="a4b5d-161">**取得 \_ X \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-161">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="a4b5d-162">**取得 \_ Y \_ LPARAM**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-162">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="a4b5d-163">**取得 \_ 輪子 \_ DELTA \_ WPARAM**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-163">**GET\_WHEEL\_DELTA\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_wheel_delta_wparam)
</dt> <dt>

<span data-ttu-id="a4b5d-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a4b5d-164">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a4b5d-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a4b5d-165">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a4b5d-166">**滑鼠 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-166">**mouse\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-mouse_event)
</dt> <dt>

<span data-ttu-id="a4b5d-167">**概念**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-167">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a4b5d-168">滑鼠輸入</span><span class="sxs-lookup"><span data-stu-id="a4b5d-168">Mouse Input</span></span>](mouse-input.md)
</dt> <dt>

<span data-ttu-id="a4b5d-169">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-169">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="a4b5d-170">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-170">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> <dt>

[<span data-ttu-id="a4b5d-171">**MAKEPOINTS**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-171">**MAKEPOINTS**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-makepoints)
</dt> <dt>

<span data-ttu-id="a4b5d-172">[**點**](/previous-versions//dd162808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a4b5d-172">[**POINTS**](/previous-versions//dd162808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a4b5d-173">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="a4b5d-173">**SystemParametersInfo**</span></span>](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

