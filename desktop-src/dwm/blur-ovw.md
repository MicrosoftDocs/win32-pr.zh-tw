---
title: DWM 模糊背後總覽
description: 其中一個桌面視窗管理員 (DWM) 效果的簽章是透明且模糊的非工作區。 DWM Api 可讓應用程式將這些效果套用到其最上層視窗的工作區。
ms.assetid: bdf0f8bd-e399-4244-ae39-460f09a16f3c
keywords:
- 桌面視窗管理員 (DWM) ，模糊後變效果
- DWM (桌面視窗管理員) ，模糊後變效果
- 模糊後變效果
- 透明效果
- 透明玻璃效果
- 桌面視窗管理員 (DWM) ，半透明效果
- DWM (桌面視窗管理員) ，半透明效果
- 桌面視窗管理員 (DWM) 、透明玻璃效果
- DWM (桌面視窗管理員) 、透明玻璃效果
- 桌面視窗管理員 (DWM) ，將視窗框架擴充到工作區
- DWM (桌面視窗管理員) ，將視窗框架擴充到工作區
- 將視窗框架擴充到工作區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fcf7378cfcaff93aa9a54ce399890ec1bfd8cc1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023991"
---
# <a name="dwm-blur-behind-overview"></a><span data-ttu-id="6d9c4-116">DWM 模糊背後總覽</span><span class="sxs-lookup"><span data-stu-id="6d9c4-116">DWM Blur Behind Overview</span></span>

<span data-ttu-id="6d9c4-117">其中一個桌面視窗管理員 (DWM) 效果的簽章是透明且模糊的非工作區。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-117">One of the signature Desktop Window Manager (DWM) effects is a translucent and blurred non-client area.</span></span> <span data-ttu-id="6d9c4-118">DWM Api 可讓應用程式將這些效果套用到其最上層視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-118">The DWM APIs enable applications to apply these effects to the client area of their top-level windows.</span></span>

> [!Note]  
> <span data-ttu-id="6d9c4-119">Windows Vista Home Basic edition 不支援透明的半透明效果。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-119">Windows Vista Home Basic edition does not support the transparent glass effect.</span></span> <span data-ttu-id="6d9c4-120">通常會在其他 Windows 版本上以透明半透明效果轉譯的區域會轉譯為不透明。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-120">Areas that would typically render with the transparent glass effect on other Windows editions are rendered as opaque.</span></span>
> <span data-ttu-id="6d9c4-121">從 Windows 8 開始，呼叫此函式並不會造成模糊效果，因為轉譯視窗的方式中的樣式變更。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-121">Beginning with Windows 8, calling this function doesn't result in the blur effect, due to a style change in the way windows are rendered.</span></span>


 

<span data-ttu-id="6d9c4-122">本主題討論 DWM 啟用的下列用戶端模糊背後案例。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-122">This topic discusses the following client blur-behind scenarios that the DWM enables.</span></span>

-   [<span data-ttu-id="6d9c4-123">將模糊新增至工作區的特定區域</span><span class="sxs-lookup"><span data-stu-id="6d9c4-123">Adding Blur to a Specific Region of the Client Area</span></span>](#adding-blur-to-a-specific-region-of-the-client-area)
-   [<span data-ttu-id="6d9c4-124">將視窗框架擴充到工作區</span><span class="sxs-lookup"><span data-stu-id="6d9c4-124">Extending the Window Frame into the Client Area</span></span>](#extending-the-window-frame-into-the-client-area)
-   [<span data-ttu-id="6d9c4-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d9c4-125">Related topics</span></span>](#related-topics)

## <a name="adding-blur-to-a-specific-region-of-the-client-area"></a><span data-ttu-id="6d9c4-126">將模糊新增至工作區的特定區域</span><span class="sxs-lookup"><span data-stu-id="6d9c4-126">Adding Blur to a Specific Region of the Client Area</span></span>

<span data-ttu-id="6d9c4-127">應用程式可將模糊效果套用到視窗的整個用戶端區域後方，或套用至特定的子領域。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-127">An application can apply the blur effect behind the whole client region of the window or to a specific subregion.</span></span> <span data-ttu-id="6d9c4-128">這可讓應用程式新增樣式的路徑和搜尋列，與應用程式的其餘部分以視覺化方式區分。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-128">This enables applications to add styled path and search bars that are visually separate from the rest of the application.</span></span>

<span data-ttu-id="6d9c4-129">此案例中使用的 API 是 [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow)函式，它會利用常數和 [**Dwm \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)結構 [**背後的 dwm 模糊**](dwm-bb-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-129">The API used in this scenario is the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function, which makes use of the [**DWM Blur Behind Constants**](dwm-bb-constants.md) and the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure.</span></span>

<span data-ttu-id="6d9c4-130">下列範例函式 `EnableBlurBehind` 說明如何將模糊後端效果套用至整個視窗。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-130">The following example function, `EnableBlurBehind`, illustrates how to apply the blur-behind effect to the whole window.</span></span>


```
HRESULT EnableBlurBehind(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Create and populate the blur-behind structure.
    DWM_BLURBEHIND bb = {0};

    // Specify blur-behind and blur region.
    bb.dwFlags = DWM_BB_ENABLE;
    bb.fEnable = true;
    bb.hRgnBlur = NULL;

    // Enable blur-behind.
    hr = DwmEnableBlurBehindWindow(hwnd, &bb);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="6d9c4-131">請注意， **Null** 是在 *hRgnBlur* 參數中指定。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-131">Note that **NULL** is specified in the *hRgnBlur* parameter.</span></span> <span data-ttu-id="6d9c4-132">這會告知 DWM 將模糊套用到整個視窗後方。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-132">This tells the DWM to apply the blur behind the whole window.</span></span>

<span data-ttu-id="6d9c4-133">下圖說明套用至整個視窗的模糊後端效果。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-133">The following image illustrates the blur-behind effect applied to the whole window.</span></span>

![套用至視窗的模糊後端效果](images/dwm-blurbehindwindow.png)

<span data-ttu-id="6d9c4-135">若要將模糊套用到子領域後方，請將有效的區域控制碼 (HRGN) 套用至 [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)結構的 **hRgnBlur** 成員，然後將 **DWM \_ BB \_ BLURREGION** 旗標加入 **dwFlags** 成員中。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-135">To apply the blur behind a subregion, apply a valid region handle (HRGN) to the **hRgnBlur** member of the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure and add the **DWM\_BB\_BLURREGION** flag to the **dwFlags** member.</span></span>

<span data-ttu-id="6d9c4-136">當您將模糊後端效果套用至視窗的子領域時，視窗的 Alpha 色板會用於 nonblurred 區域。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-136">When you apply the blur-behind effect to a subregion of the window, the alpha channel of the window is used for the nonblurred area.</span></span> <span data-ttu-id="6d9c4-137">這可能會導致視窗的 nonblurred 區域出現非預期的透明度。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-137">This can cause an unexpected transparency in the nonblurred region of a window.</span></span> <span data-ttu-id="6d9c4-138">因此，當您將模糊效果套用至子領域時，請務必小心。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-138">Therefore, be careful when you apply a blur effect to a subregion.</span></span>

## <a name="extending-the-window-frame-into-the-client-area"></a><span data-ttu-id="6d9c4-139">將視窗框架擴充到工作區</span><span class="sxs-lookup"><span data-stu-id="6d9c4-139">Extending the Window Frame into the Client Area</span></span>

<span data-ttu-id="6d9c4-140">應用程式可以將視窗框架的模糊擴充到工作區。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-140">An application can extend the blur of the window frame into the client area.</span></span> <span data-ttu-id="6d9c4-141">當您使用停駐的工具列套用視窗背後的模糊效果，或以視覺化方式將控制項與應用程式的其餘部分分開時，這會很有用。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-141">This is useful when you apply the blur effect behind a window with a docked toolbar or visually separate controls from the rest of an application.</span></span> <span data-ttu-id="6d9c4-142">這項功能是由 [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 函數所公開。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-142">This functionality is exposed by the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) function.</span></span>

<span data-ttu-id="6d9c4-143">若要使用 [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea)來啟用模糊，請使用 [**邊界**](/windows/win32/api/uxtheme/ns-uxtheme-margins) 結構來指出要延伸至工作區的程度。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-143">To enable blur by using [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea), use the [**MARGINS**](/windows/win32/api/uxtheme/ns-uxtheme-margins) structure to indicate how much to extend into the client area.</span></span> <span data-ttu-id="6d9c4-144">下列範例函式會將 `ExtendIntoClientBottom` 非用戶端框架底部的模糊擴充功能切換至工作區。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-144">The following example function, `ExtendIntoClientBottom`, toggles the blur extension on the bottom of the non-client frame into the client area.</span></span>


```
HRESULT ExtendIntoClientBottom(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Set the margins, extending the bottom margin.
    MARGINS margins = {0,0,0,25};

    // Extend the frame on the bottom of the client area.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="6d9c4-145">下圖說明延伸至用戶端區域底部的模糊後端效果。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-145">The following image illustrates the blur-behind effect extended into the bottom of the client area.</span></span>

![顯示延伸至用戶端區域底部之模糊後變效果的影像](images/dwm-extendedbottom.png)

<span data-ttu-id="6d9c4-147">也可透過 [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) 方法使用，這是「半透明工作表」的效果，其中模糊效果會套用至視窗的整個表面，而不會有可見的視窗框線。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-147">Also available through the [**DwmExtendFrameIntoClientArea**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmextendframeintoclientarea) method is the "sheet of glass" effect, where the blur effect is applied to the whole surface of the window without a visible window border.</span></span> <span data-ttu-id="6d9c4-148">下列範例示範在不使用視窗框線的情況下呈現用戶端區域的效果。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-148">The following example demonstrates this effect where the client area is rendered without a window border.</span></span>


```
HRESULT ExtendIntoClientAll(HWND hwnd)
{
    HRESULT hr = S_OK;

    // Negative margins have special meaning to DwmExtendFrameIntoClientArea.
    // Negative margins create the "sheet of glass" effect, where the client 
    // area is rendered as a solid surface without a window border.
    MARGINS margins = {-1};

    // Extend the frame across the whole window.
    hr = DwmExtendFrameIntoClientArea(hwnd,&margins);
    if (SUCCEEDED(hr))
    {
        // ...
    }
    return hr;
}
```



<span data-ttu-id="6d9c4-149">下圖說明「半透明工作表」視窗樣式的模糊背後。</span><span class="sxs-lookup"><span data-stu-id="6d9c4-149">The following image illustrates the blur-behind in the "sheet of glass" window style.</span></span>

![說明「半透明工作表」視窗樣式中模糊背後效果的影像](images/dwm-sheetofglass.png)

## <a name="related-topics"></a><span data-ttu-id="6d9c4-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d9c4-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d9c4-152">桌面視窗管理員概觀</span><span class="sxs-lookup"><span data-stu-id="6d9c4-152">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="6d9c4-153">Enable and Control DWM Composition (啟用並控制 DWM 組合)</span><span class="sxs-lookup"><span data-stu-id="6d9c4-153">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="6d9c4-154">效能考慮和最佳作法</span><span class="sxs-lookup"><span data-stu-id="6d9c4-154">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 