---
title: 啟用及控制 DWM 組合
description: 桌面視窗管理員 (DWM) 撰寫 Api 提供數個函式，可用來設定及查詢 DWM 所使用的基本資訊。
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_composition_ovw.htm
keywords:
- 桌面視窗管理員 (DWM) ，組合
- DWM (桌面視窗管理員) ，組合
- 組合
- 桌面電腦群組合
- 著色
- 非用戶端區域呈現
- 桌面視窗管理員 (DWM) 、顏色標示
- DWM (桌面視窗管理員) 、顏色標示
- 桌面視窗管理員 (DWM) 、非用戶端區域呈現
- DWM (桌面視窗管理員) 、非用戶端區域呈現
- 桌面視窗管理員 (DWM) 、訊息
- DWM (桌面視窗管理員) ，訊息
- 傳訊
ms.topic: article
ms.date: 05/30/2019
ms.openlocfilehash: 8d7654f479896002b4bc65df613fab9506caf2a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840644"
---
# <a name="enable-and-control-dwm-composition"></a><span data-ttu-id="97023-116">啟用及控制 DWM 組合</span><span class="sxs-lookup"><span data-stu-id="97023-116">Enable and control DWM composition</span></span>

<span data-ttu-id="97023-117">桌面視窗管理員 (DWM) 撰寫 Api 提供數個函式，可用來設定及查詢 DWM 所使用的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="97023-117">The Desktop Window Manager (DWM) composition APIs provide several functions for setting and querying for basic information that is used by the DWM.</span></span> <span data-ttu-id="97023-118">這些 Api 可讓您查詢及變更撰寫狀態。</span><span class="sxs-lookup"><span data-stu-id="97023-118">These APIs enable you to query and change the composition state.</span></span> <span data-ttu-id="97023-119">此外，您可以針對不同的 DWM 視窗屬性，設定和查詢轉譯原則。</span><span class="sxs-lookup"><span data-stu-id="97023-119">Additionally, you can set and query the rendering policy for different DWM window attributes.</span></span>

## <a name="retrieving-colorization-information"></a><span data-ttu-id="97023-120">正在抓取顏色標示資訊</span><span class="sxs-lookup"><span data-stu-id="97023-120">Retrieving colorization information</span></span>

<span data-ttu-id="97023-121">視窗的非用戶端區域色彩是由目前的系統色彩主題所決定。</span><span class="sxs-lookup"><span data-stu-id="97023-121">The color of the non-client region of a window is determined by the current system color theme.</span></span> <span data-ttu-id="97023-122">顏色標示值是透過 DWM Api 提供，可讓您的應用程式比對用戶端 UI 與系統色彩主題。</span><span class="sxs-lookup"><span data-stu-id="97023-122">The colorization value is provided through the DWM APIs to enable your application to match client UI with the system color theme.</span></span>

<span data-ttu-id="97023-123">若要存取這個顏色標示值並監視色彩變更，請使用 [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) 函式和 [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="97023-123">To access this colorization value, and monitor the color change, use the [**DwmGetColorizationColor**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetcolorizationcolor) function and the [**WM_DWMCOLORIZATIONCOLORCHANGED**](wm-dwmcolorizationcolorchanged.md) message.</span></span>

<span data-ttu-id="97023-124">這個範例示範如何處理色彩變更的訊息，以及如何存取新的色彩。</span><span class="sxs-lookup"><span data-stu-id="97023-124">This example demonstrates how to handle the color changed message and access the new color.</span></span>

```cpp
...
case WM_DWMCOLORIZATIONCOLORCHANGED:
{
    DWORD newColorizationColor{ (DWORD)wParam };
    BOOL isBlendedWithOpacity{ (BOOL)lParam };
}
break;
...
```

## <a name="controlling-non-client-region-rendering"></a><span data-ttu-id="97023-125">控制非用戶端區域呈現</span><span class="sxs-lookup"><span data-stu-id="97023-125">Controlling non-client region rendering</span></span>

<span data-ttu-id="97023-126">DWM 啟用的兩項視覺效果，是視窗的非用戶端區域的透明度，以及轉換效果。</span><span class="sxs-lookup"><span data-stu-id="97023-126">Two of the visual effects that DWM enables are transparency of the non-client region of a window, and transition effects.</span></span> <span data-ttu-id="97023-127">您的應用程式可能必須基於樣式或相容性的理由，停用或重新啟用這些效果。</span><span class="sxs-lookup"><span data-stu-id="97023-127">Your application might have to disable or re-enable these effects for styling or compatibility reasons.</span></span> <span data-ttu-id="97023-128">下列函式可用來管理透明度和轉換效果的行為。</span><span class="sxs-lookup"><span data-stu-id="97023-128">The following functions are used to manage transparency and transition effect behavior.</span></span>

- [<span data-ttu-id="97023-129">**DwmGetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="97023-129">**DwmGetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute)
- [<span data-ttu-id="97023-130">**DwmSetWindowAttribute**</span><span class="sxs-lookup"><span data-stu-id="97023-130">**DwmSetWindowAttribute**</span></span>](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute)

<span data-ttu-id="97023-131">若要取得應用程式視窗的目前非用戶端轉譯狀態，請呼叫 [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) ，並將 *dwAttribute* 設定為 [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)。</span><span class="sxs-lookup"><span data-stu-id="97023-131">To retrieve the current non-client rendering state for an application's window, call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with *dwAttribute* set to [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute).</span></span> <span data-ttu-id="97023-132">您可以從 [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute)的檔中看到，當您將該旗標傳遞給 **DwmGetWindowAttribute** 時，所抓取的屬性值為 **BOOL** 類型。</span><span class="sxs-lookup"><span data-stu-id="97023-132">As you can see from the documentation for [**DWMWA_NCRENDERING_ENABLED**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute), when you pass that flag to **DwmGetWindowAttribute**, the retrieved attribute value is of type **BOOL**.</span></span> <span data-ttu-id="97023-133">不同的旗標會使 **DwmGetWindowAttribute** 傳回不同類型的值。</span><span class="sxs-lookup"><span data-stu-id="97023-133">Different flags cause **DwmGetWindowAttribute** to return values of different types.</span></span> <span data-ttu-id="97023-134">以下是程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="97023-134">Here's a code example.</span></span>

```cpp
BOOL isNCRenderingEnabled{ FALSE };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_NCRENDERING_ENABLED,
    &isNCRenderingEnabled,
    sizeof(isNCRenderingEnabled));
```

<span data-ttu-id="97023-135">下一個範例示範如何搭配使用 [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) 旗標與 **DwmGetWindowAttribute** ，以抓取視窗的擴充框架界限矩形。</span><span class="sxs-lookup"><span data-stu-id="97023-135">This next example shows how to use the [**DWMWA_EXTENDED_FRAME_BOUNDS**](/windows/desktop/api/dwmapi/ne-dwmapi-dwmwindowattribute) flag with **DwmGetWindowAttribute** to retrieve the extended frame bounds rectangle of a window.</span></span> <span data-ttu-id="97023-136">該旗標的檔告訴我們，所抓取的屬性值是 **RECT** 型別。</span><span class="sxs-lookup"><span data-stu-id="97023-136">The documentation for that flag tells us that the retrieved attribute value is of type **RECT**.</span></span>

```cpp
RECT extendedFrameBounds{ 0,0,0,0 };
HRESULT hr = ::DwmGetWindowAttribute(hWnd,
    DWMWA_EXTENDED_FRAME_BOUNDS,
    &extendedFrameBounds,
    sizeof(extendedFrameBounds));
```

> [!NOTE]
> <span data-ttu-id="97023-137">當您使用不同屬性的旗標呼叫 [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) 時，請遵循上面所示的相同程式設計模式。</span><span class="sxs-lookup"><span data-stu-id="97023-137">Follow the same programming pattern shown above when you call [**DwmGetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmgetwindowattribute) with flags for different attributes.</span></span> <span data-ttu-id="97023-138">[**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)列舉主題指出每個旗標的資料列中，您應該在 **DwmGetWindowAttribute** 的 *pvAttribute* 參數中傳遞指標的數值型別。</span><span class="sxs-lookup"><span data-stu-id="97023-138">The [**DWMWINDOWATTRIBUTE**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) enumeration topic indicates, in the row for each flag, what type of value you should pass a pointer to in the *pvAttribute* parameter for **DwmGetWindowAttribute**.</span></span> <span data-ttu-id="97023-139">*CbAttribute* 參數包含該物件的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="97023-139">The *cbAttribute* parameter contains the size, in bytes, of that object.</span></span>

<span data-ttu-id="97023-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) 可讓您的應用程式設定非工作區呈現原則。</span><span class="sxs-lookup"><span data-stu-id="97023-140">[**DwmSetWindowAttribute**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmsetwindowattribute) enables your application to set the non-client area rendering policy.</span></span> <span data-ttu-id="97023-141">該函式也會決定您的應用程式應該如何處理 DWM 轉換效果。</span><span class="sxs-lookup"><span data-stu-id="97023-141">That function also determines how your application should handle DWM transition effects.</span></span>

<span data-ttu-id="97023-142">下一個範例會停用非工作區呈現。</span><span class="sxs-lookup"><span data-stu-id="97023-142">This next example disables non-client area rendering.</span></span> <span data-ttu-id="97023-143">這會導致任何先前對 [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) 或 [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 的呼叫停用。</span><span class="sxs-lookup"><span data-stu-id="97023-143">This causes any previous calls to [DwmEnableBlurBehindWindow](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenableblurbehindwindow) or to [DwmExtendFrameIntoClientArea](/windows/desktop/api/dwmapi/nf-dwmapi-dwmextendframeintoclientarea) to be disabled.</span></span>

```
HRESULT DisableNCRendering(HWND hWnd)
{
    HRESULT hr = S_OK;

    DWMNCRENDERINGPOLICY ncrp = DWMNCRP_DISABLED;

    // Disable non-client area rendering on the window.
    hr = ::DwmSetWindowAttribute(hWnd,
        DWMWA_NCRENDERING_POLICY,
        &ncrp,
        sizeof(ncrp));

    if (SUCCEEDED(hr))
    {
        // ...
    }

    return hr;
}
```

<span data-ttu-id="97023-144">除了控制非工作區呈現之外， [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) 還可以控制 DWM 轉換效果。</span><span class="sxs-lookup"><span data-stu-id="97023-144">In addition to controlling the non-client area rendering, [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) can also control DWM transition effects.</span></span> <span data-ttu-id="97023-145">您可以使用 **DWMWA \_ 轉換 \_ FORCEDISABLED** 做為 *dwAttribute* 參數來設定轉換行為。</span><span class="sxs-lookup"><span data-stu-id="97023-145">You can set transition behavior by using **DWMWA\_TRANSITIONS\_FORCEDISABLED** as the *dwAttribute* parameter.</span></span>

## <a name="messages"></a><span data-ttu-id="97023-146">訊息</span><span class="sxs-lookup"><span data-stu-id="97023-146">Messages</span></span>

<span data-ttu-id="97023-147">下列訊息提供 DWM 事件的通知。</span><span class="sxs-lookup"><span data-stu-id="97023-147">The following messages provide notification of DWM events.</span></span> <span data-ttu-id="97023-148">這些訊息可以用來監視變更，例如撰寫狀態變更和系統色彩主題變更。</span><span class="sxs-lookup"><span data-stu-id="97023-148">These messages can be used to monitor changes such as composition state changes and system color theme changes.</span></span>

- [<span data-ttu-id="97023-149">**WM \_ DWMCOLORIZATIONCOLORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="97023-149">**WM\_DWMCOLORIZATIONCOLORCHANGED**</span></span>](wm-dwmcolorizationcolorchanged.md)
- [<span data-ttu-id="97023-150">**WM \_ DWMCOMPOSITIONCHANGED**</span><span class="sxs-lookup"><span data-stu-id="97023-150">**WM\_DWMCOMPOSITIONCHANGED**</span></span>](wm-dwmcompositionchanged.md)
- [<span data-ttu-id="97023-151">**WM \_ DWMNCRENDERINGCHANGED**</span><span class="sxs-lookup"><span data-stu-id="97023-151">**WM\_DWMNCRENDERINGCHANGED**</span></span>](wm-dwmncrenderingchanged.md)
- [<span data-ttu-id="97023-152">**WM \_ DWMWINDOWMAXIMIZEDCHANGE**</span><span class="sxs-lookup"><span data-stu-id="97023-152">**WM\_DWMWINDOWMAXIMIZEDCHANGE**</span></span>](wm-dwmwindowmaximizedchange.md)

## <a name="disabling-dwm-composition-windows7-and-earlier"></a><span data-ttu-id="97023-153">停用 Windows 7 和舊版)  (的 DWM 組合</span><span class="sxs-lookup"><span data-stu-id="97023-153">Disabling DWM composition (Windows 7 and earlier)</span></span>

> [!WARNING]
> <span data-ttu-id="97023-154">本節中的資訊僅適用于 Windows 7 和舊版系統。</span><span class="sxs-lookup"><span data-stu-id="97023-154">The info in this section applies only to Windows 7 and earlier systems.</span></span>

<span data-ttu-id="97023-155">因為 DWM 會使用圖形處理器 (GPU) 進行桌面撰寫，所以您的應用程式可能必須停用 DWM 以提供相容性。</span><span class="sxs-lookup"><span data-stu-id="97023-155">Because DWM uses the graphics processing unit (GPU) for desktop composition, your application might have to disable DWM for compatibility.</span></span> <span data-ttu-id="97023-156">完全控制桌面的應用程式（例如在全螢幕模式中執行的遊戲）必須判斷 DWM 是否已啟用，如果是，則會將它停用。</span><span class="sxs-lookup"><span data-stu-id="97023-156">Applications that take full control of the desktop, such as games that run in full-screen mode, must determine whether the DWM is enabled and if it is, disable it.</span></span> <span data-ttu-id="97023-157">若要這樣做，需要兩個函數。</span><span class="sxs-lookup"><span data-stu-id="97023-157">To do this, two functions are needed.</span></span>

- [<span data-ttu-id="97023-158">**DwmIsCompositionEnabled**</span><span class="sxs-lookup"><span data-stu-id="97023-158">**DwmIsCompositionEnabled**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmiscompositionenabled)
- [<span data-ttu-id="97023-159">**DwmEnableComposition**</span><span class="sxs-lookup"><span data-stu-id="97023-159">**DwmEnableComposition**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)

<span data-ttu-id="97023-160">將 *fEnable* 設定為 **dwm \_ ec \_ DISABLECOMPOSITION** 的 [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)呼叫會停用 DWM 組合，直到呼叫進程關閉為止，或藉由呼叫 **DwmEnableComposition** （將 *fEnable* 設定為 **DWM \_ EC \_ ENABLECOMPOSITION**）來重新啟用組合。</span><span class="sxs-lookup"><span data-stu-id="97023-160">A call to [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition) with *fEnable* set to **DWM\_EC\_DISABLECOMPOSITION** disables DWM composition until either the calling process has shut down, or composition has been re-enabled by calling **DwmEnableComposition** with *fEnable* set to **DWM\_EC\_ENABLECOMPOSITION**.</span></span> <span data-ttu-id="97023-161">當所有已停用組合的應用程式都已關閉，或藉由呼叫 **DwmEnableComposition** 手動重新啟用組合時，DWM 組合就會自動重新開機。</span><span class="sxs-lookup"><span data-stu-id="97023-161">DWM composition restarts automatically as soon as all applications that have disabled composition have either shut down or have manually re-enabled composition by calling **DwmEnableComposition**.</span></span>

> [!NOTE]  
> <span data-ttu-id="97023-162">當應用程式嘗試直接繪製至主顯示器介面時，DWM 會自動停用組合。</span><span class="sxs-lookup"><span data-stu-id="97023-162">The DWM automatically disables composition when an application attempts to draw directly to the primary display surface.</span></span> <span data-ttu-id="97023-163">在該應用程式放開主要裝置介面之前，將會停用組合。</span><span class="sxs-lookup"><span data-stu-id="97023-163">Composition will be disabled until the primary device surface is released by that application.</span></span>
