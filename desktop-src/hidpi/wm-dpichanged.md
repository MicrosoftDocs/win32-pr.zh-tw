---
title: 'WM_DPICHANGED 訊息 (WinUser .h) '
description: 當視窗的有效點 (DPI) 變更時傳送。
ms.assetid: 97C458F2-89CD-45FF-ABEE-F158A3BCE0B8
keywords:
- WM_DPICHANGED 訊息高 DPI
topic_type:
- apiref
api_name:
- WM_DPICHANGED
api_location:
- WinUser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aafbce1e784e1f205f0d32e045785125c1fb5aaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685991"
---
# <a name="wm_dpichanged-message"></a><span data-ttu-id="02377-104">WM \_ DPICHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="02377-104">WM\_DPICHANGED message</span></span>

<span data-ttu-id="02377-105">當視窗的有效點 (DPI) 變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="02377-105">Sent when the effective dots per inch (dpi) for a window has changed.</span></span> <span data-ttu-id="02377-106">DPI 是視窗的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="02377-106">The DPI is the scale factor for a window.</span></span> <span data-ttu-id="02377-107">有多個事件可能會造成 DPI 變更。</span><span class="sxs-lookup"><span data-stu-id="02377-107">There are multiple events that can cause the DPI to change.</span></span> <span data-ttu-id="02377-108">下列清單指出可能的 DPI 變更原因。</span><span class="sxs-lookup"><span data-stu-id="02377-108">The following list indicates the possible causes for the change in DPI.</span></span>

-   <span data-ttu-id="02377-109">視窗會移至具有不同 DPI 的新監視器。</span><span class="sxs-lookup"><span data-stu-id="02377-109">The window is moved to a new monitor that has a different DPI.</span></span>
-   <span data-ttu-id="02377-110">主控視窗的監視器 DPI 會變更。</span><span class="sxs-lookup"><span data-stu-id="02377-110">The DPI of the monitor hosting the window changes.</span></span>

<span data-ttu-id="02377-111">視窗的目前 DPI 永遠等於 **WM \_ DPICHANGED** 所傳送的最後一個 DPI。</span><span class="sxs-lookup"><span data-stu-id="02377-111">The current DPI for a window always equals the last DPI sent by **WM\_DPICHANGED**.</span></span> <span data-ttu-id="02377-112">這是視窗應該針對感知 DPI 變更的執行緒進行調整的比例因數。</span><span class="sxs-lookup"><span data-stu-id="02377-112">This is the scale factor that the window should be scaling to for threads that are aware of DPI changes.</span></span>


```C++
#define WM_DPICHANGED       0x02E0
```



## <a name="parameters"></a><span data-ttu-id="02377-113">參數</span><span class="sxs-lookup"><span data-stu-id="02377-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02377-114">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02377-114">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02377-115">*WParam* 的 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))包含新的視窗 DPI 的 Y 軸值。</span><span class="sxs-lookup"><span data-stu-id="02377-115">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of the *wParam* contains the Y-axis value of the new dpi of the window.</span></span> <span data-ttu-id="02377-116">*WParam* 的 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))包含新的視窗 DPI 的 X 軸值。</span><span class="sxs-lookup"><span data-stu-id="02377-116">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) of the *wParam* contains the X-axis value of the new DPI of the window.</span></span> <span data-ttu-id="02377-117">例如，96、120、144或192。</span><span class="sxs-lookup"><span data-stu-id="02377-117">For example, 96, 120, 144, or 192.</span></span> <span data-ttu-id="02377-118">針對 Windows 應用程式，X 軸和 Y 軸的值是相同的。</span><span class="sxs-lookup"><span data-stu-id="02377-118">The values of the X-axis and the Y-axis are identical for Windows apps.</span></span>

</dd> <dt>

<span data-ttu-id="02377-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02377-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="02377-120">[**矩形**](/windows/desktop/api/windef/ns-windef-rect)結構的指標，提供針對新的 DPI 縮放的目前視窗的建議大小和位置。</span><span class="sxs-lookup"><span data-stu-id="02377-120">A pointer to a [**RECT**](/windows/desktop/api/windef/ns-windef-rect) structure that provides a suggested size and position of the current window scaled for the new DPI.</span></span> <span data-ttu-id="02377-121">預期應用程式會根據 *lParam* 在處理此訊息時所提供的建議，重新調整視窗的位置並調整其大小。</span><span class="sxs-lookup"><span data-stu-id="02377-121">The expectation is that apps will reposition and resize windows based on the suggestions provided by *lParam* when handling this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02377-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="02377-122">Return value</span></span>

<span data-ttu-id="02377-123">如果應用程式處理此訊息，它應該會傳回零。</span><span class="sxs-lookup"><span data-stu-id="02377-123">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="02377-124">備註</span><span class="sxs-lookup"><span data-stu-id="02377-124">Remarks</span></span>

<span data-ttu-id="02377-125">這則訊息只適用于每個監視器感知 **\_ \_ \_ DPI \_ 感知** 應用程式的處理常式，或 **\_ \_ 每個 \_ 監視器 \_ 感知執行緒的 DPI 感知** 。</span><span class="sxs-lookup"><span data-stu-id="02377-125">This message is only relevant for **PROCESS\_PER\_MONITOR\_DPI\_AWARE** applications or **DPI\_AWARENESS\_PER\_MONITOR\_AWARE** threads.</span></span> <span data-ttu-id="02377-126">如果您的最上層視窗或進程以 **DPI** **感知或系統 DPI 感知** 的形式執行，則可能會收到特定 DPI 變更的相關資訊，但在這些情況下，可以放心忽略。</span><span class="sxs-lookup"><span data-stu-id="02377-126">It may be received on certain DPI changes if your top-level window or process is running as **DPI unaware** or **system DPI aware**, but in those situations it can be safely ignored.</span></span> <span data-ttu-id="02377-127">如需不同類型感知的詳細資訊，請參閱 [**處理 \_ DPI \_ 感知**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) 和 [**DPI \_ 感知**](/windows/desktop/api/windef/ne-windef-dpi_awareness)。</span><span class="sxs-lookup"><span data-stu-id="02377-127">For more information about the different types of awareness, see [**PROCESS\_DPI\_AWARENESS**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness) and [**DPI\_AWARENESS**](/windows/desktop/api/windef/ne-windef-dpi_awareness).</span></span> <span data-ttu-id="02377-128">舊版 Windows 需要 DPI 感知才能系結至應用程式的層級。</span><span class="sxs-lookup"><span data-stu-id="02377-128">Older versions of Windows required DPI awareness to be tied at the level of an application.</span></span> <span data-ttu-id="02377-129">這些應用程式會使用 **進程 \_ DPI \_ 感知**。</span><span class="sxs-lookup"><span data-stu-id="02377-129">Those apps use **PROCESS\_DPI\_AWARENESS**.</span></span> <span data-ttu-id="02377-130">目前，DPI 感知系結至執行緒和個別的視窗，而不是整個應用程式。</span><span class="sxs-lookup"><span data-stu-id="02377-130">Currently, DPI awareness is tied to threads and individual windows rather than the entire application.</span></span> <span data-ttu-id="02377-131">這些應用程式會使用 **DPI \_ 感知**。</span><span class="sxs-lookup"><span data-stu-id="02377-131">These apps use **DPI\_AWARENESS**.</span></span>

<span data-ttu-id="02377-132">調整您的應用程式時，您只需要使用 X 軸或 Y 軸的值，因為它們是相同的。</span><span class="sxs-lookup"><span data-stu-id="02377-132">You only need to use either the X-axis or the Y-axis value when scaling your application since they are the same.</span></span>

<span data-ttu-id="02377-133">為了正確處理此訊息，您將需要根據 *lParam* 和使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)所提供的建議，調整視窗的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="02377-133">In order to handle this message correctly, you will need to resize and reposition your window based on the suggestions provided by *lParam* and using [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos).</span></span> <span data-ttu-id="02377-134">如果您沒有這樣做，您的視窗就會隨著新監視器上的其他專案而成長或縮小。</span><span class="sxs-lookup"><span data-stu-id="02377-134">If you do not do this, your window will grow or shrink with respect to everything else on the new monitor.</span></span> <span data-ttu-id="02377-135">例如，如果使用者使用多個監視器，並將您的視窗從 96 DPI 監視器拖曳至 192 DPI 監視器，則在 192 DPI 監視器上的視窗會顯示為與其他專案很大的一半。</span><span class="sxs-lookup"><span data-stu-id="02377-135">For example, if a user is using multiple monitors and drags your window from a 96 DPI monitor to a 192 DPI monitor, your window will appear to be half as large with respect to other items on the 192 DPI monitor.</span></span>

<span data-ttu-id="02377-136">DPI 的基底值定義為 **使用者 \_ 預設 \_ 畫面 \_ DPI** ，其設定為96。</span><span class="sxs-lookup"><span data-stu-id="02377-136">The base value of DPI is defined as **USER\_DEFAULT\_SCREEN\_DPI** which is set to 96.</span></span> <span data-ttu-id="02377-137">若要判斷監視的縮放比例，請採用 DPI 值，並依 **使用者的 \_ 預設 \_ 螢幕 \_ DPI** 來分割。</span><span class="sxs-lookup"><span data-stu-id="02377-137">To determine the scaling factor for a monitor, take the DPI value and divide by **USER\_DEFAULT\_SCREEN\_DPI**.</span></span> <span data-ttu-id="02377-138">下表提供一些範例 DPI 值和相關聯的縮放因數。</span><span class="sxs-lookup"><span data-stu-id="02377-138">The following table provides some sample DPI values and associated scaling factors.</span></span>



| <span data-ttu-id="02377-139">DPI 值</span><span class="sxs-lookup"><span data-stu-id="02377-139">DPI value</span></span> | <span data-ttu-id="02377-140">調整百分比</span><span class="sxs-lookup"><span data-stu-id="02377-140">Scaling percentage</span></span> |
|-----------|--------------------|
| <span data-ttu-id="02377-141">96</span><span class="sxs-lookup"><span data-stu-id="02377-141">96</span></span>        | <span data-ttu-id="02377-142">100%</span><span class="sxs-lookup"><span data-stu-id="02377-142">100%</span></span>               |
| <span data-ttu-id="02377-143">120</span><span class="sxs-lookup"><span data-stu-id="02377-143">120</span></span>       | <span data-ttu-id="02377-144">125%</span><span class="sxs-lookup"><span data-stu-id="02377-144">125%</span></span>               |
| <span data-ttu-id="02377-145">144</span><span class="sxs-lookup"><span data-stu-id="02377-145">144</span></span>       | <span data-ttu-id="02377-146">150%</span><span class="sxs-lookup"><span data-stu-id="02377-146">150%</span></span>               |
| <span data-ttu-id="02377-147">192</span><span class="sxs-lookup"><span data-stu-id="02377-147">192</span></span>       | <span data-ttu-id="02377-148">200%</span><span class="sxs-lookup"><span data-stu-id="02377-148">200%</span></span>               |



 

<span data-ttu-id="02377-149">下列範例提供範例 DPI 變更處理常式。</span><span class="sxs-lookup"><span data-stu-id="02377-149">The following example provides a sample DPI change handler.</span></span>


```C++
    case WM_DPICHANGED:
    {
        g_dpi = HIWORD(wParam);
        UpdateDpiDependentFontsAndResources();

        RECT* const prcNewWindow = (RECT*)lParam;
        SetWindowPos(hWnd,
            NULL,
            prcNewWindow ->left,
            prcNewWindow ->top,
            prcNewWindow->right - prcNewWindow->left,
            prcNewWindow->bottom - prcNewWindow->top,
            SWP_NOZORDER | SWP_NOACTIVATE);
        break;
    }
```



<span data-ttu-id="02377-150">下列程式碼會以線性方式將值從 100% (96 DPI) 調整為 *g \_ DPI* 所定義的任意 DPI。</span><span class="sxs-lookup"><span data-stu-id="02377-150">The following code linearly scales a value from 100% (96 DPI) to an arbitrary DPI defined by *g\_dpi*.</span></span>


```C++
    INT iBorderWidth100 = 5;
    iBorderWidth = MulDiv(iBorderWidth100, g_dpi, USER_DEFAULT_SCREEN_DPI);
```



<span data-ttu-id="02377-151">調整值的替代方式是將 DPI 值轉換成縮放比例，然後使用該值。</span><span class="sxs-lookup"><span data-stu-id="02377-151">An alternative way to scale a value is to convert the DPI value into a scale factor and use that.</span></span>


```C++
    INT iBorderWidth100 = 5;
    FLOAT fscale = (float) g_dpi / USER_DEFAULT_SCREEN_DPI;
    iBorderWidth = iBorderWidth100 * fscale;
```



## <a name="requirements"></a><span data-ttu-id="02377-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="02377-152">Requirements</span></span>



| <span data-ttu-id="02377-153">需求</span><span class="sxs-lookup"><span data-stu-id="02377-153">Requirement</span></span> | <span data-ttu-id="02377-154">值</span><span class="sxs-lookup"><span data-stu-id="02377-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="02377-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02377-155">Minimum supported client</span></span><br/> | <span data-ttu-id="02377-156">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02377-156">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="02377-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02377-157">Minimum supported server</span></span><br/> | <span data-ttu-id="02377-158">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02377-158">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="02377-159">標頭</span><span class="sxs-lookup"><span data-stu-id="02377-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="02377-160"><dt>WinUser。h</dt></span><span class="sxs-lookup"><span data-stu-id="02377-160"><dt>WinUser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02377-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02377-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02377-162">**DPI \_ 感知**</span><span class="sxs-lookup"><span data-stu-id="02377-162">**DPI\_AWARENESS**</span></span>](/windows/desktop/api/windef/ne-windef-dpi_awareness)
</dt> <dt>

[<span data-ttu-id="02377-163">**進程 \_ DPI \_ 感知**</span><span class="sxs-lookup"><span data-stu-id="02377-163">**PROCESS\_DPI\_AWARENESS**</span></span>](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)
</dt> </dl>

 

