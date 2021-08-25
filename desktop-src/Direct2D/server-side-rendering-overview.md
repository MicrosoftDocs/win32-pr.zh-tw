---
title: 使用 Direct2D 進行 Server-Side 轉譯
description: 描述如何使用 Direct2D 進行伺服器端轉譯。
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D，伺服器端轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65991d2437939ce7f1d218022e0c3c57649405a18e2c1b9d073635b5b37d1a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917197"
---
# <a name="using-direct2d-for-server-side-rendering"></a>使用 Direct2D 進行 Server-Side 轉譯

Direct2D 非常適合需要 Windows server 上進行伺服器端轉譯的圖形應用程式。 本總覽說明使用 Direct2D 進行伺服器端轉譯的基本概念。 它包含下列區段：

-   [Server-Side 轉譯的需求](#requirements-for-server-side-rendering)
-   [可用 Api 的選項](#options-for-available-apis)
    -   [GDI](#gdi)
    -   [GDI+](#gdi)
    -   [Direct2D](#using-direct2d-for-server-side-rendering)
-   [如何使用 Direct2D 進行 Server-Side 轉譯](#how-to-use-direct2d-for-server-side-rendering)
    -   [軟體轉譯](#software-rendering)
    -   [多執行緒](#multithreading)
    -   [產生點陣圖檔案](#generating-a-bitmap-file)
-   [結論](#conclusion)
-   [相關主題](#related-topics)

## <a name="requirements-for-server-side-rendering"></a>Server-Side 轉譯的需求

以下是圖表伺服器的一般案例：圖表和圖形會轉譯在伺服器上，並以點陣圖形式傳遞，以回應 Web 要求。 伺服器可能具有低端圖形介面卡，或沒有任何圖形卡。

此案例會顯示三個應用程式需求。 首先，應用程式必須有效率地處理多個並行要求，尤其是在多核心伺服器上。 第二，應用程式必須在具有低終端圖形配接器或沒有圖形配接器的伺服器上執行時，使用軟體轉譯。 最後，應用程式必須在會話0中以服務的形式執行，如此就不需要使用者登入。 如需會話0的詳細資訊，請參閱[Windows 中的服務與驅動程式的會話0隔離影響](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx)。

## <a name="options-for-available-apis"></a>可用 Api 的選項

伺服器端呈現有三個選項： GDI、GDI+ 和 Direct2D。 如同 GDI 和 GDI+，Direct2D 是原生2d 轉譯 API，可讓應用程式更充分掌控圖形裝置的使用。 此外，Direct2D 可唯一支援單一執行緒和多執行緒處理站。 下列各節會根據繪圖品質和多執行緒伺服器端轉譯來比較每個 API。

### <a name="gdi"></a>GDI

不同于 Direct2D 和 GDI+，GDI 不支援高品質的繪圖功能。 比方說，GDI 不支援建立平滑線的消除鋸齒功能，而且只對透明度的支援有限。 根據 Windows 7 和 Windows Server 2008 R2 上的圖形效能測試結果，Direct2D 會比 gdi 更有效率地進行調整，儘管在 gdi 中重新設計鎖定。 如需這些測試結果的詳細資訊，請參閱[工程 Windows 7 圖形效能](/archive/blogs/e7/engineering-windows-7-graphics-performance)。

此外，使用 GDI 的應用程式限制為每個進程10240個 GDI 控制碼，以及每個會話65536個 GDI 控制碼。 原因是內部 Windows 使用16位字組來儲存每個會話之控制碼的索引。

### <a name="gdi"></a>GDI+

雖然 GDI+ 支援高品質繪圖的消除鋸齒和 Alpha 混色，但伺服器案例的 GDI+ 主要問題是它不支援在會話0中執行。 因為會話0只支援非互動式功能，所以直接或間接與顯示裝置互動的函式將會收到錯誤。 函式的特定範例不僅包括處理顯示裝置的程式，也包括間接處理設備磁碟機的函式。

類似于 GDI，GDI+ 受限於其鎖定機制。 GDI+ 中的鎖定機制與舊版中的 Windows 7 和 Windows Server 2008 R2 相同。

### <a name="direct2d"></a>Direct2D

Direct2D 是一種硬體加速、即時模式、2D 圖形 API，可提供高效能和高品質的呈現。 它提供單一執行緒和多執行緒處理站，以及進行課程更精細的軟體轉譯的線性調整。

若要這樣做，Direct2D 會定義根 factory 介面。 作為規則，在處理站上建立的物件只能與其他從相同 factory 建立的物件搭配使用。 呼叫端可以在建立時要求單一執行緒或多執行緒處理站。 如果要求單一執行緒 factory，則不會執行任何鎖定執行緒。 如果呼叫端要求多執行緒處理站，則每次呼叫 Direct2D 時，就會取得 factory 範圍的執行緒鎖定。

此外，Direct2D 中線程的鎖定比在 GDI 和 GDI+ 中更細微，因此增加執行緒的數目會對效能造成最大的影響。

## <a name="how-to-use-direct2d-for-server-side-rendering"></a>如何使用 Direct2D 進行 Server-Side 轉譯

下列各節說明如何使用軟體轉譯、如何以最佳方式使用單一執行緒和多執行緒處理站，以及如何繪製複雜的繪圖並將其儲存至檔案。

### <a name="software-rendering"></a>軟體轉譯

伺服器端應用程式會藉由建立 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標來使用軟體轉譯，而轉譯目標型別會設定為 D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 軟體或 D2D1 轉譯 \_ \_ 目標 \_ 類型 \_ 預設值。 如需 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標的詳細資訊，請參閱 [**ID2D1Factory：： CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) 方法。如需呈現目標型別的詳細資訊，請參閱 [**D2D1 轉譯 \_ \_ 目標 \_ 類型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type)。

### <a name="multithreading"></a>多執行緒

瞭解如何線上程之間建立和共用處理站和轉譯目標，可能會大幅影響應用程式的效能。 下列三個圖形顯示三種不同的方法。 [圖 3] 顯示最佳的方法。

![使用單一轉譯目標 direct2d 多執行緒圖表。](images/server-side-rendering-1.png)

在 [圖 1] 中，不同的執行緒共用相同的 factory 和相同的呈現目標。 當多個執行緒同時變更共用轉譯目標的狀態（例如同時設定轉換矩陣）時，此方法可能會導致無法預期的結果。 由於 Direct2D 中的內部鎖定並不會同步處理共用資源（例如轉譯目標），因此此方法可能會導致執行緒1中的 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 呼叫失敗，因為線上程2中， **BeginDraw** 呼叫已使用共用轉譯目標。

![具有多個呈現目標的 direct2d 多執行緒圖表。](images/server-side-rendering-2.png)

為了避免在 [圖 1] 中發生無法預期的結果，[圖 2] 顯示每個執行緒都有自己呈現目標的多執行緒處理站。 這種方法可以運作，但它會有效地當作單一執行緒應用程式。 原因是，factory 範圍鎖定只適用于繪圖作業層級，而相同處理站中的所有繪圖呼叫則會進行序列化。 如此一來，當執行緒2在執行另一個繪製呼叫的過程中，執行緒1會遭到封鎖而無法進入繪圖呼叫。

![具有多個 factory 和多個呈現目標的 direct2d 多執行緒圖表。](images/server-side-rendering-3.png)

[圖 3] 顯示最佳的方法，其中會使用單一執行緒的處理站和單一執行緒的呈現目標。 由於使用單一執行緒處理站時不會執行任何鎖定，因此每個執行緒中的繪圖作業可以同時執行，以達到最佳效能。

### <a name="generating-a-bitmap-file"></a>產生點陣圖檔案

若要使用軟體呈現來產生點陣圖檔案，請使用 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標。 使用 [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) 將點陣圖寫入檔案。 使用 [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) 將點陣圖編碼為指定的影像格式。 下列程式碼範例示範如何繪製下列影像並將其儲存至檔案。

![範例輸出影像。](images/saveasimagefile-sample.png)

這個程式碼範例會先建立 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 和 [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) 轉譯目標。 然後，它會呈現包含一些文字的繪圖、代表一個小時玻璃的路徑幾何，以及將小時的半透明轉譯成 WIC 點陣圖。 然後，它會使用 [IWICStream：： InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) 將點陣圖儲存至檔案。 如果您的應用程式需要將點陣圖儲存在記憶體中，請改用 [IWICStream：： InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) 。 最後，它會使用 [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) 來編碼點陣圖。


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a>結論

如上所示，使用 Direct2D 進行伺服器端轉譯相當簡單明瞭。 此外，它還提供高品質且高度可並行的轉譯，可在伺服器的低許可權環境中執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 