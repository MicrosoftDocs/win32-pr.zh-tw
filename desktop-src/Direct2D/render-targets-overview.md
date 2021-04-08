---
title: 轉譯目標總覽
description: 描述不同類型的 Direct2D 轉譯目標，以及如何使用它們。
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D，轉譯目標
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933366"
---
# <a name="render-targets-overview"></a>轉譯目標總覽

轉譯目標是繼承自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 介面的資源。 轉譯目標會建立用來繪製和執行實際繪圖作業的資源。 本主題說明不同類型的 Direct2D 轉譯目標，以及如何使用它們。

-   [呈現目標](#render-targets-overview)
    -   [呈現目標功能](#render-target-features)
    -   [呈現目標資源](#render-target-resources)
    -   [繪製命令](#drawing-commands)
    -   [錯誤處理](#error-handling)
-   [範例：將內容呈現至視窗](#example-render-content-to-a-window)

## <a name="render-targets"></a>呈現目標

轉譯目標是繼承自 [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) 介面的資源。 轉譯目標會建立用來繪製和執行實際繪圖作業的資源。 有幾種轉譯目標可用於以下列方式呈現圖形：

-   [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 物件會將內容轉譯至視窗。
-   [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) 物件會轉譯成 GDI 裝置內容。
-   點陣圖轉譯目標物件會將內容轉譯為非螢幕點陣圖。
-   DXGI 轉譯目標物件會轉譯成 DXGI 介面，以搭配 Direct3D 使用。

由於轉譯目標是與特定轉譯裝置相關聯，因此它是裝置相依的資源，如果裝置已移除，就會停止運作。

### <a name="render-target-features"></a>呈現目標功能

您可以指定轉譯目標是否使用硬體加速，以及遠端顯示是否由本機或遠端電腦所呈現。 您可以設定呈現目標，以進行別名或反鋸齒呈現。 針對具有大量基本專案的轉譯場景，開發人員也可以在別名模式中轉譯2D 圖形，並使用 D3D 多取樣消除鋸齒來達成更高的擴充性。

轉譯目標也可以將繪圖作業分組為 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 介面所代表的圖層。 當轉譯畫面格時，圖層會用來收集要組合在一起的繪圖作業。 在某些案例中，這可能是轉譯成點陣圖轉譯目標的實用替代方式，然後重複使用點陣圖內容，因為階層式配置成本低於 [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)。

轉譯目標可以建立與本身相容的新轉譯目標，這適用于中繼的非畫面轉譯，同時保留原始上設定的各種呈現目標屬性。

您也可以在 Direct2D 轉譯目標上使用 GDI 來轉譯，方法是在 [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)的轉譯目標上呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，此方法上具有 [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc)和 [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc)方法，可用來取出 GDI 裝置內容。 只有當轉譯目標是使用 [**D2D1 轉譯 \_ \_ 目標 \_ 使用 \_ GDI \_ 相容**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) 旗標集建立時，才可以透過 gdi 轉譯。 這適用于主要以 Direct2D 轉譯，但具有擴充性模型或其他需要能夠以 GDI 轉譯之舊版內容的應用程式。 如需詳細資訊，請參閱 [Direct2D 和 GDI 互通性總覽](direct2d-and-gdi-interoperation-overview.md)。

### <a name="render-target-resources"></a>呈現目標資源

就像 factory 一樣，轉譯目標可以建立繪圖資源。 轉譯目標所建立的任何資源都是與裝置相關的資源 (就像呈現目標) 一樣。 轉譯目標可建立下列類型的資源：

-   點陣圖
-   筆刷
-   圖層
-   網狀

### <a name="drawing-commands"></a>繪製命令

若要轉譯內容，您可以使用呈現目標繪製方法。 開始繪製之前，請先呼叫 [**ID2D1RenderTarget：： BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法。 完成繪製之後，您會呼叫 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。 在這些呼叫之間，您會使用 Draw 和 Fill 方法來呈現繪圖資源。 大部分的繪圖和填滿方法都採用圖形 (基本或幾何) ，以及用來填滿或大綱圖形的筆刷。

轉譯目標提供剪下、套用不透明度遮罩，以及轉換座標空間的方法。

Direct2D 使用左方座標系統：正 X 軸的值會繼續往右，y 軸的正值則會往下進行。

### <a name="error-handling"></a>錯誤處理

轉譯目標繪製命令不會指出要求的作業是否成功。 若要找出是否有繪圖錯誤，請呼叫轉譯目標 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法或 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法來取得 **HRESULT**。

## <a name="example-render-content-to-a-window"></a>範例：將內容呈現至視窗

下列範例會使用 [**CreateHwndRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) 方法來建立 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)。


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



下一個範例會使用 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) ，在視窗中繪製文字。


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



此範例中省略了程式碼。

 

 