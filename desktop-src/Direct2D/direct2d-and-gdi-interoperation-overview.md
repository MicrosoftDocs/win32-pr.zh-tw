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
ms.openlocfilehash: 951bebc9ea7ca63496a9cdc93fa33ddb74817661e7f5bc072b55d207bfcbdeb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918234"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a>Direct2D 和 GDI 互通性總覽

本主題說明如何搭配使用 Direct2D 和 [GDI](/windows/desktop/gdi/windows-gdi) 。 有兩種方式可以將 Direct2D 與 GDI 結合：您可以將 GDI 內容寫入 Direct2D 的 GDI 相容轉譯目標，也可以將 Direct2D 的內容寫入 [ (DC) 的 Gdi 裝置 ](/windows/desktop/gdi/device-contexts)內容。

本主題包含下列各節。

-   [必要條件](#prerequisites)
-   [將 Direct2D 內容繪製至 GDI 裝置內容](#draw-direct2d-content-to-a-gdi-device-context)
-   [Windows 的 ID2D1DCRenderTargets、GDI 轉換和由右至左語言組建](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [將 GDI 內容繪製至 Direct2D GDI-Compatible 呈現目標](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

本總覽假設您已經熟悉基本的 Direct2D 繪圖作業。 如需教學課程，請參閱 [Direct2D 快速入門](direct2d-quickstart.md)。 它也假設您已熟悉 GDI 繪圖作業。

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a>將 Direct2D 內容繪製至 GDI 裝置內容

若要將 Direct2D 內容繪製至 GDI DC，請使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)。 若要建立 DC 呈現目標，請使用 [**ID2D1Factory：： CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) 方法。 這個方法會採用兩個參數。

第一個參數（ [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 結構）指定轉譯、遠端處理、DPI、像素格式和使用方式資訊。 若要讓 DC 轉譯目標使用 GDI，請將 [DXGI 格式] 設定為 [ [dxgi \_ 格式 \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ] 和 [Alpha] 模式，以 [**D2D1 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) 的預乘或 **D2D1 \_ Alpha \_ 模式 \_ 忽略**。

第二個參數是接收 DC 呈現目標參考之指標的位址。

下列程式碼會建立 DC 呈現目標。


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



在上述程式碼中 *，m \_ pD2DFactory* 是指向 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)的指標，而 *m \_ pDCRT* 是 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)的指標。

您必須使用其 [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) 方法，將它與 GDI dc 產生關聯，才能使用 DC 轉譯目標來呈現。 每次使用不同的 DC，或您想要繪製的區域大小變更時，就會執行此動作。

[**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc)方法會採用兩個參數： *hDC* 和 *pSubRect*。 *HDC* 參數提供可接收轉譯目標輸出的裝置內容控制碼。 *PSubRect* 參數是一個矩形，可描述呈現內容的裝置內容部分。 DC 轉譯目標會更新其大小，以符合 *pSubRect* 所描述的裝置內容區域是否會變更大小。

下列程式碼會將 DC 系結至 DC 呈現目標。


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
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



將 DC 轉譯目標與 DC 建立關聯之後，您就可以使用它來繪製。 下列程式碼會使用 DC 來繪製 Direct2D 和 GDI 內容。


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



這段程式碼會產生如下圖所示的輸出 (已新增注解，以醒目提示 Direct2D 和 GDI 轉譯之間的差異。 ) 

![以 direct2d 和 gdi 轉譯的兩個圓形圖表圖例](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a>Windows 的 ID2D1DCRenderTargets、GDI 轉換和由右至左語言組建

當您使用 [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)時，它會將 Direct2D 內容轉譯為內部點陣圖，然後將點陣圖轉譯為具有 GDI 的 DC。

GDI 可能會透過 [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) 方法，將 gdi 轉換 () 或其他效果套用到轉譯目標所使用的相同 DC，在這種情況下，gdi 會轉換 Direct2D 所產生的點陣圖。 使用 GDI 轉換來轉換 Direct2D 內容有可能會降低輸出的視覺品質，因為您要轉換的點陣圖已計算消除鋸齒和子圖元定位。

例如，假設您使用呈現目標來繪製包含反鋸齒幾何和文字的場景。 如果您使用 GDI 轉換將刻度轉換套用至 DC，並調整場景的大小，使其大於10倍，您將會看到 pixelization 和鋸齒狀邊緣。  (如果您使用 Direct2D 來套用類似的轉換，場景的視覺品質將不會降級。 ) 

在某些情況下，GDI 可能無法明顯地執行可能會降低 Direct2D 內容品質的額外處理。 例如，從右至左 (RTL) 的 Windows 組建， [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)轉譯的內容可能會在 GDI 複製到其目的地時水準反轉。 內容是否真的反轉，取決於 DC 目前的設定。

視轉譯的內容類型而定，您可能會想要避免反轉。 如果 Direct2D 內容包含 ClearType 文字，此反轉將會降低文字品質。

您可以使用 [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI 函數來控制 RTL 轉譯行為。 若要防止鏡像，請呼叫 **SetLayout** GDI 函數，並將配置 **\_ BITMAPORIENTATIONPRESERVED** 指定為第二個參數的唯一值 (請勿將它與配置 **\_ RTL**) 結合，如下列範例所示：


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a>將 GDI 內容繪製至 Direct2D GDI-Compatible 呈現目標

上一節說明如何將 Direct2D 內容寫入至 GDI DC。 您也可以將 GDI 內容寫入至 Direct2D 的 GDI 相容轉譯目標。 這種方法適用于主要以 Direct2D 轉譯的應用程式，但具有擴充性模型或其他需要能夠使用 GDI 轉譯的舊版內容。

若要將 GDI 內容轉譯為 Direct2D 的 GDI 相容轉譯目標，請使用 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)，其可存取可接受 GDI 繪製呼叫的裝置內容。 不同于其他介面，不會直接建立 **ID2D1GdiInteropRenderTarget** 物件。 相反地，請使用現有呈現目標實例的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法。 下列程式碼示範如何執行這項作業：


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



在上述程式碼中 *，m \_ pD2DFactory* 是指向 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)的指標，而 *m \_ pGDIRT* 是 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)的指標。

請注意，在建立 Hwnd 與 GDI 相容的轉譯目標時，會指定 [**D2D1 轉譯 \_ \_ 目標 \_ 使用 \_ GDI \_ 相容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) 旗標。 如果需要像素格式，請使用 [DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)。 如果需要 Alpha 模式，請使用 [**D2D1 的 \_ Alpha \_ 模式 \_**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ，或 **D2D1 的 \_ Alpha 模式 [ \_ \_ 略** 過]。

請注意， [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法一律會成功。 若要測試 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) 介面的方法是否適用于指定的轉譯目標，請建立 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 來指定 gdi 相容性和適當的像素格式，然後呼叫轉譯目標的 [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) 方法，以查看轉譯目標是否與 GDI 相容。

下列範例示範如何將 (GDI 內容) 的圓形圖繪製到 Hwnd GDI 相容轉譯目標。


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



程式碼會輸出如下圖所示的圖表，其中包含用來醒目提示呈現品質差異的標注。 右邊的圓形圖 (GDI 內容) 的轉譯品質低於左邊的圓形圖 (Direct2D 內容) 。 這是因為 Direct2D 能夠以消除鋸齒呈現

![在 direct2d gdi 相容轉譯目標中轉譯的兩個圓形圖表圖例](images/gdicontentind2d.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[**D2D1 \_ 轉譯 \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[GDI 裝置內容](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[GDI SDK](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 