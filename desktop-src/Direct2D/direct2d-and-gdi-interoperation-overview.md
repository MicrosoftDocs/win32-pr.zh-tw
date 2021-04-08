---
title: Direct2D 和 GDI 互通性總覽
description: 說明如何搭配使用 Direct2D 和 GDI。
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D，GDI 交互操作
- Direct2D，互通性
- 互通性，Direct2D
- '圖形裝置介面 (GDI) '
- 'GDI (圖形裝置介面) '
- '互通性、圖形裝置介面 (GDI) '
- Direct3D、互通性
- Direct3D、Direct2D 互通性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682948"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a><span data-ttu-id="7d29b-111">Direct2D 和 GDI 互通性總覽</span><span class="sxs-lookup"><span data-stu-id="7d29b-111">Direct2D and GDI Interoperability Overview</span></span>

<span data-ttu-id="7d29b-112">本主題說明如何搭配使用 Direct2D 和 [GDI](/windows/desktop/gdi/windows-gdi) 。</span><span class="sxs-lookup"><span data-stu-id="7d29b-112">This topic describes how to use Direct2D and [GDI](/windows/desktop/gdi/windows-gdi) together.</span></span> <span data-ttu-id="7d29b-113">有兩種方式可以將 Direct2D 與 GDI 結合：您可以將 GDI 內容寫入 Direct2D 的 GDI 相容轉譯目標，也可以將 Direct2D 的內容寫入 [ (DC) 的 Gdi 裝置 ](/windows/desktop/gdi/device-contexts)內容。</span><span class="sxs-lookup"><span data-stu-id="7d29b-113">There are two ways to combine Direct2D with GDI: you can write GDI content to a Direct2D GDI-compatible render target, or you can write Direct2D content to a [GDI Device Context (DC)](/windows/desktop/gdi/device-contexts).</span></span>

<span data-ttu-id="7d29b-114">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="7d29b-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="7d29b-115">先決條件</span><span class="sxs-lookup"><span data-stu-id="7d29b-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="7d29b-116">將 Direct2D 內容繪製至 GDI 裝置內容</span><span class="sxs-lookup"><span data-stu-id="7d29b-116">Draw Direct2D Content to a GDI Device Context</span></span>](#draw-direct2d-content-to-a-gdi-device-context)
-   [<span data-ttu-id="7d29b-117">Windows 的 ID2D1DCRenderTargets、GDI 轉換和由右至左語言組建</span><span class="sxs-lookup"><span data-stu-id="7d29b-117">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [<span data-ttu-id="7d29b-118">將 GDI 內容繪製至 Direct2D GDI-Compatible 呈現目標</span><span class="sxs-lookup"><span data-stu-id="7d29b-118">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [<span data-ttu-id="7d29b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d29b-119">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="7d29b-120">必要條件</span><span class="sxs-lookup"><span data-stu-id="7d29b-120">Prerequisites</span></span>

<span data-ttu-id="7d29b-121">本總覽假設您已經熟悉基本的 Direct2D 繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="7d29b-121">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="7d29b-122">如需教學課程，請參閱 [Direct2D 快速入門](direct2d-quickstart.md)。</span><span class="sxs-lookup"><span data-stu-id="7d29b-122">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="7d29b-123">它也假設您已熟悉 GDI 繪圖作業。</span><span class="sxs-lookup"><span data-stu-id="7d29b-123">It also assumes that you are familiar with GDI drawing operations.</span></span>

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a><span data-ttu-id="7d29b-124">將 Direct2D 內容繪製至 GDI 裝置內容</span><span class="sxs-lookup"><span data-stu-id="7d29b-124">Draw Direct2D Content to a GDI Device Context</span></span>

<span data-ttu-id="7d29b-125">若要將 Direct2D 內容繪製至 GDI DC，請使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)。</span><span class="sxs-lookup"><span data-stu-id="7d29b-125">To draw Direct2D content to a GDI DC, you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="7d29b-126">若要建立 DC 呈現目標，請使用 [**ID2D1Factory：： CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) 方法。</span><span class="sxs-lookup"><span data-stu-id="7d29b-126">To create a DC render target, you use the [**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) method.</span></span> <span data-ttu-id="7d29b-127">這個方法會採用兩個參數。</span><span class="sxs-lookup"><span data-stu-id="7d29b-127">This method takes two parameters.</span></span>

<span data-ttu-id="7d29b-128">第一個參數（ [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 結構）指定轉譯、遠端處理、DPI、像素格式和使用方式資訊。</span><span class="sxs-lookup"><span data-stu-id="7d29b-128">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure, specifies rendering, remoting, DPI, pixel format, and usage information.</span></span> <span data-ttu-id="7d29b-129">若要讓 DC 轉譯目標使用 GDI，請將 [DXGI 格式] 設定為 [ [dxgi \_ 格式 \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ] 和 [Alpha] 模式，以 [**D2D1 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的預乘或 **D2D1 \_ Alpha \_ 模式 \_ 忽略**。</span><span class="sxs-lookup"><span data-stu-id="7d29b-129">To enable the DC render target to work with GDI, set the DXGI format to [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) and the alpha mode to [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="7d29b-130">第二個參數是接收 DC 呈現目標參考之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="7d29b-130">The second parameter is the address of the pointer that receive the DC render target reference.</span></span>

<span data-ttu-id="7d29b-131">下列程式碼會建立 DC 呈現目標。</span><span class="sxs-lookup"><span data-stu-id="7d29b-131">The following code creates a DC render target.</span></span>


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



<span data-ttu-id="7d29b-132">在上述程式碼中 *，m \_ pD2DFactory* 是指向 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)的指標，而 *m \_ pDCRT* 是 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)的指標。</span><span class="sxs-lookup"><span data-stu-id="7d29b-132">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pDCRT* is a pointer to an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span>

<span data-ttu-id="7d29b-133">您必須使用其 [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) 方法，將它與 GDI dc 產生關聯，才能使用 DC 轉譯目標來呈現。</span><span class="sxs-lookup"><span data-stu-id="7d29b-133">Before you can render with the DC render target, you must use its [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method to associate it with a GDI DC.</span></span> <span data-ttu-id="7d29b-134">每次使用不同的 DC，或您想要繪製的區域大小變更時，就會執行此動作。</span><span class="sxs-lookup"><span data-stu-id="7d29b-134">You do this each time you use a different DC, or the size of the area you want to draw to changes.</span></span>

<span data-ttu-id="7d29b-135">[**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc)方法會採用兩個參數： *hDC* 和 *pSubRect*。</span><span class="sxs-lookup"><span data-stu-id="7d29b-135">The [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method takes two parameters, *hDC* and *pSubRect*.</span></span> <span data-ttu-id="7d29b-136">*HDC* 參數提供可接收轉譯目標輸出的裝置內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="7d29b-136">The *hDC* parameter provides a handle to the device context that receives the output of the render target.</span></span> <span data-ttu-id="7d29b-137">*PSubRect* 參數是一個矩形，可描述呈現內容的裝置內容部分。</span><span class="sxs-lookup"><span data-stu-id="7d29b-137">The *pSubRect* parameter is a rectangle that describes the portion of the device context to which content is rendered.</span></span> <span data-ttu-id="7d29b-138">DC 轉譯目標會更新其大小，以符合 *pSubRect* 所描述的裝置內容區域是否會變更大小。</span><span class="sxs-lookup"><span data-stu-id="7d29b-138">The DC render target updates its size to match the device context area described by *pSubRect*, should it change size.</span></span>

<span data-ttu-id="7d29b-139">下列程式碼會將 DC 系結至 DC 呈現目標。</span><span class="sxs-lookup"><span data-stu-id="7d29b-139">The following code binds a DC to a DC render target.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d29b-140">C++</span><span class="sxs-lookup"><span data-stu-id="7d29b-140">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="7d29b-141">將 DC 轉譯目標與 DC 建立關聯之後，您就可以使用它來繪製。</span><span class="sxs-lookup"><span data-stu-id="7d29b-141">After you associate the DC render target with a DC, you can use it to draw.</span></span> <span data-ttu-id="7d29b-142">下列程式碼會使用 DC 來繪製 Direct2D 和 GDI 內容。</span><span class="sxs-lookup"><span data-stu-id="7d29b-142">The following code draws Direct2D and GDI content using a DC.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="7d29b-143">這段程式碼會產生如下圖所示的輸出 (已新增注解，以醒目提示 Direct2D 和 GDI 轉譯之間的差異。 ) </span><span class="sxs-lookup"><span data-stu-id="7d29b-143">This code produces outputs as shown in the following illustration (callouts have been added to highlight the difference between Direct2D and GDI rendering.)</span></span>

![以 direct2d 和 gdi 轉譯的兩個圓形圖表圖例](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a><span data-ttu-id="7d29b-145">Windows 的 ID2D1DCRenderTargets、GDI 轉換和由右至左語言組建</span><span class="sxs-lookup"><span data-stu-id="7d29b-145">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>

<span data-ttu-id="7d29b-146">當您使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)時，它會將 Direct2D 內容轉譯為內部點陣圖，然後將點陣圖轉譯為具有 GDI 的 DC。</span><span class="sxs-lookup"><span data-stu-id="7d29b-146">When you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI.</span></span>

<span data-ttu-id="7d29b-147">GDI 可能會透過 [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) 方法，將 gdi 轉換 () 或其他效果套用到轉譯目標所使用的相同 DC，在這種情況下，gdi 會轉換 Direct2D 所產生的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="7d29b-147">It's possible for GDI to apply a GDI transform (through the [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D.</span></span> <span data-ttu-id="7d29b-148">使用 GDI 轉換來轉換 Direct2D 內容有可能會降低輸出的視覺品質，因為您要轉換的點陣圖已計算消除鋸齒和子圖元定位。</span><span class="sxs-lookup"><span data-stu-id="7d29b-148">Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.</span></span>

<span data-ttu-id="7d29b-149">例如，假設您使用呈現目標來繪製包含反鋸齒幾何和文字的場景。</span><span class="sxs-lookup"><span data-stu-id="7d29b-149">For example, suppose you use the render target to draw a scene that contains antialiased geometries and text.</span></span> <span data-ttu-id="7d29b-150">如果您使用 GDI 轉換將刻度轉換套用至 DC，並調整場景的大小，使其大於10倍，您將會看到 pixelization 和鋸齒狀邊緣。</span><span class="sxs-lookup"><span data-stu-id="7d29b-150">If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges.</span></span> <span data-ttu-id="7d29b-151"> (如果您使用 Direct2D 來套用類似的轉換，場景的視覺品質將不會降級。 ) </span><span class="sxs-lookup"><span data-stu-id="7d29b-151">(If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)</span></span>

<span data-ttu-id="7d29b-152">在某些情況下，GDI 可能無法明顯地執行可能會降低 Direct2D 內容品質的額外處理。</span><span class="sxs-lookup"><span data-stu-id="7d29b-152">In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content.</span></span> <span data-ttu-id="7d29b-153">例如，從右至左 (RTL) 的視窗組建， [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 轉譯的內容可能會在 GDI 複製到其目的地時以水準方式反轉。</span><span class="sxs-lookup"><span data-stu-id="7d29b-153">For example, on a right-to-left (RTL) build of Windows, content rendered by an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) might be horizontally inverted when GDI copies it to its destination.</span></span> <span data-ttu-id="7d29b-154">內容是否真的反轉，取決於 DC 目前的設定。</span><span class="sxs-lookup"><span data-stu-id="7d29b-154">Whether the content is actually inverted depends on the current settings of the DC.</span></span>

<span data-ttu-id="7d29b-155">視轉譯的內容類型而定，您可能會想要避免反轉。</span><span class="sxs-lookup"><span data-stu-id="7d29b-155">Depending on the type of content being rendered, you might want to prevent the inversion.</span></span> <span data-ttu-id="7d29b-156">如果 Direct2D 內容包含 ClearType 文字，此反轉將會降低文字品質。</span><span class="sxs-lookup"><span data-stu-id="7d29b-156">If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.</span></span>

<span data-ttu-id="7d29b-157">您可以使用 [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI 函數來控制 RTL 轉譯行為。</span><span class="sxs-lookup"><span data-stu-id="7d29b-157">You can control RTL rendering behavior by using the [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI function.</span></span> <span data-ttu-id="7d29b-158">若要防止鏡像，請呼叫 **SetLayout** GDI 函數，並將配置 **\_ BITMAPORIENTATIONPRESERVED** 指定為第二個參數的唯一值 (請勿將它與配置 **\_ RTL**) 結合，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="7d29b-158">To prevent the mirroring, call the **SetLayout** GDI function and specify **LAYOUT\_BITMAPORIENTATIONPRESERVED** as the only value for the second parameter (do not combine it with **LAYOUT\_RTL**), as shown in the following example:</span></span>


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a><span data-ttu-id="7d29b-159">將 GDI 內容繪製至 Direct2D GDI-Compatible 呈現目標</span><span class="sxs-lookup"><span data-stu-id="7d29b-159">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>

<span data-ttu-id="7d29b-160">上一節說明如何將 Direct2D 內容寫入至 GDI DC。</span><span class="sxs-lookup"><span data-stu-id="7d29b-160">The previous section describes how to write Direct2D content to a GDI DC.</span></span> <span data-ttu-id="7d29b-161">您也可以將 GDI 內容寫入至 Direct2D 的 GDI 相容轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="7d29b-161">You can also write GDI content to a Direct2D GDI-compatible render target.</span></span> <span data-ttu-id="7d29b-162">這種方法適用于主要以 Direct2D 轉譯的應用程式，但具有擴充性模型或其他需要能夠使用 GDI 轉譯的舊版內容。</span><span class="sxs-lookup"><span data-stu-id="7d29b-162">This approach is useful for applications that primarily render with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span>

<span data-ttu-id="7d29b-163">若要將 GDI 內容轉譯為 Direct2D 的 GDI 相容轉譯目標，請使用 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)，其可存取可接受 GDI 繪製呼叫的裝置內容。</span><span class="sxs-lookup"><span data-stu-id="7d29b-163">To render GDI content to a Direct2D GDI-compatible render target, use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which provides access to a device context that can accept GDI draw calls.</span></span> <span data-ttu-id="7d29b-164">不同于其他介面，不會直接建立 **ID2D1GdiInteropRenderTarget** 物件。</span><span class="sxs-lookup"><span data-stu-id="7d29b-164">Unlike other interfaces, an **ID2D1GdiInteropRenderTarget** object is not created directly.</span></span> <span data-ttu-id="7d29b-165">相反地，請使用現有呈現目標實例的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法。</span><span class="sxs-lookup"><span data-stu-id="7d29b-165">Instead, use the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of an existing render target instance.</span></span> <span data-ttu-id="7d29b-166">下列程式碼示範如何執行這項作業：</span><span class="sxs-lookup"><span data-stu-id="7d29b-166">The following code shows how to do this:</span></span>


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



<span data-ttu-id="7d29b-167">在上述程式碼中 *，m \_ pD2DFactory* 是指向 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)的指標，而 *m \_ pGDIRT* 是 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)的指標。</span><span class="sxs-lookup"><span data-stu-id="7d29b-167">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pGDIRT* is a pointer to an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span></span>

<span data-ttu-id="7d29b-168">請注意，在建立 Hwnd 與 GDI 相容的轉譯目標時，會指定 [**D2D1 轉譯 \_ \_ 目標 \_ 使用 \_ GDI \_ 相容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) 旗標。</span><span class="sxs-lookup"><span data-stu-id="7d29b-168">Notice that the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag is specified when creating the Hwnd GDI-compatible render target.</span></span> <span data-ttu-id="7d29b-169">如果需要像素格式，請使用 [DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)。</span><span class="sxs-lookup"><span data-stu-id="7d29b-169">If a pixel format is required, use [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="7d29b-170">如果需要 Alpha 模式，請使用 [**D2D1 的 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ，或 **D2D1 的 \_ Alpha 模式 [ \_ \_ 略** 過]。</span><span class="sxs-lookup"><span data-stu-id="7d29b-170">If an alpha mode is required, use [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="7d29b-171">請注意， [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法一律會成功。</span><span class="sxs-lookup"><span data-stu-id="7d29b-171">Note that the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method always succeeds.</span></span> <span data-ttu-id="7d29b-172">若要測試 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) 介面的方法是否適用于指定的轉譯目標，請建立 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 來指定 gdi 相容性和適當的像素格式，然後呼叫轉譯目標的 [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) 方法，以查看轉譯目標是否與 GDI 相容。</span><span class="sxs-lookup"><span data-stu-id="7d29b-172">To test whether the [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) interface's methods will work for a given render target, create a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) that specifies GDI compatibility and the appropriate pixel format, and then call the render target's [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) method to see whether the render target is GDI-compatible.</span></span>

<span data-ttu-id="7d29b-173">下列範例示範如何將 (GDI 內容) 的圓形圖繪製到 Hwnd GDI 相容轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="7d29b-173">The following example shows how to draw a pie chart (GDI content) to the Hwnd GDI-compatible render target.</span></span>


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



<span data-ttu-id="7d29b-174">程式碼會輸出如下圖所示的圖表，其中包含用來醒目提示呈現品質差異的標注。</span><span class="sxs-lookup"><span data-stu-id="7d29b-174">The code outputs charts as shown in the following illustration with callouts to highlight the rendering quality difference.</span></span> <span data-ttu-id="7d29b-175">右邊的圓形圖 (GDI 內容) 的轉譯品質低於左邊的圓形圖 (Direct2D 內容) 。</span><span class="sxs-lookup"><span data-stu-id="7d29b-175">The right pie chart (GDI content) has lower rendering quality than the left pie chart (Direct2D content).</span></span> <span data-ttu-id="7d29b-176">這是因為 Direct2D 能夠以消除鋸齒呈現</span><span class="sxs-lookup"><span data-stu-id="7d29b-176">This is because Direct2D is capable of rendering with antialiasing</span></span>

![在 direct2d gdi 相容轉譯目標中轉譯的兩個圓形圖表圖例](images/gdicontentind2d.png)

## <a name="related-topics"></a><span data-ttu-id="7d29b-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d29b-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d29b-179">**ID2D1Factory::CreateDCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="7d29b-179">**ID2D1Factory::CreateDCRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[<span data-ttu-id="7d29b-180">**ID2D1DCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="7d29b-180">**ID2D1DCRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[<span data-ttu-id="7d29b-181">**ID2D1GdiInteropRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="7d29b-181">**ID2D1GdiInteropRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[<span data-ttu-id="7d29b-182">**D2D1 \_ 轉譯 \_ 目標 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="7d29b-182">**D2D1\_RENDER\_TARGET\_PROPERTIES**</span></span>](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[<span data-ttu-id="7d29b-183">GDI 裝置內容</span><span class="sxs-lookup"><span data-stu-id="7d29b-183">GDI Device Contexts</span></span>](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[<span data-ttu-id="7d29b-184">GDI SDK</span><span class="sxs-lookup"><span data-stu-id="7d29b-184">GDI SDK</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 