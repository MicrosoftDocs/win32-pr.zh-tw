---
title: Direct2D 快速入門
description: 摘要說明使用 Direct2D 進行繪製所需的步驟，並提供範例程式碼。
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D，繪製矩形程式碼範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f9c4f7ee6ca99feb3cf7169a59ce73ff3b8f8c62c08ddad88b9e5acf5d9a814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260062"
---
# <a name="direct2d-quickstart"></a>Direct2D 快速入門

Direct2D 是原生程式碼的立即模式 API，可用於建立2D 圖形。 本主題說明如何在典型的 Win32 應用程式中使用 Direct2D 來繪製至 **HWND**。

> [!Note]  
> 如果您想要建立使用 Direct2D 的 Windows Store 應用程式，請參閱[Windows 8 主題的 Direct2D 快速入門](direct2d-quickstart-with-device-context.md)。

 

本主題包含下列幾節：

-   [繪製簡單的矩形](#drawing-a-simple-rectangle)
-   [步驟1： Include Direct2D 標頭](#step-1-include-direct2d-header)
-   [步驟2：建立 ID2D1Factory](#step-2-create-an-id2d1factory)
-   [步驟3：建立 ID2D1HwndRenderTarget](#step-3-create-an-id2d1hwndrendertarget)
-   [步驟4：建立筆刷](#step-4-create-a-brush)
-   [步驟5：繪製矩形](#step-5-draw-the-rectangle)
-   [步驟6：釋放資源](#step-6-release-resources)
-   [建立簡單的 Direct2D 應用程式](#create-a-simple-direct2d-application)
-   [相關主題](#related-topics)

## <a name="drawing-a-simple-rectangle"></a>繪製簡單的矩形

若要使用 [GDI](/windows/desktop/gdi/windows-gdi)繪製矩形，您可以處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，如下列程式碼所示。


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



使用 Direct2D 繪製相同矩形的程式碼很類似：它會建立繪圖資源、描述要繪製的圖形、繪製圖形，然後釋放繪圖資源。 接下來的各節將詳細說明每個步驟。

## <a name="step-1-include-direct2d-header"></a>步驟1： Include Direct2D 標頭

除了 Win32 應用程式所需的標頭之外，還包括 d2d1 標頭。

## <a name="step-2-create-an-id2d1factory"></a>步驟2：建立 ID2D1Factory

任何 Direct2D 範例所做的第一件事，就是建立 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)。


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)介面是使用 Direct2D 的起點;使用 **ID2D1Factory** 來建立 Direct2D 資源。

當您建立 factory 時，您可以指定它是多個還是單一執行緒。  (如需多執行緒處理站的詳細資訊，請參閱 [**ID2D1Factory 參考頁面**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)上的備註。 ) 此範例會建立單一執行緒 factory。

一般情況下，您的應用程式應建立一次 factory，並將其保留在應用程式的存留期內。

## <a name="step-3-create-an-id2d1hwndrendertarget"></a>步驟3：建立 ID2D1HwndRenderTarget

建立 factory 之後，請使用它來建立轉譯目標。


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



轉譯目標是一種裝置，可執行繪圖作業，並建立與裝置相關的繪圖資源，例如筆刷。 不同類型的呈現目標會轉譯成不同的裝置。 上述範例會使用 [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)，它會呈現在螢幕的某個部分。

可能的話，轉譯目標會使用 GPU 來加速轉譯作業和建立繪圖資源。 否則，轉譯目標會使用 CPU 來處理轉譯指令和建立資源。  (當您建立轉譯目標時，可以使用 [**D2D1 轉譯 \_ \_ 目標 \_ 類型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 旗標來修改此行為。 ) 

[**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))方法會採用三個參數。 第一個參數是 [**D2D1 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) 結構，可指定遠端顯示選項、是否強制轉譯目標轉譯為軟體或硬體，以及 DPI。 此範例中的程式碼會使用 [**D2D1：： RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper 函式來接受預設轉譯目標屬性。

第二個參數（ [**D2D1 \_ HWND \_ 轉譯 \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) 結構）指定要呈現內容的 **HWND** 、轉譯目標的初始大小 (以圖元為單位) ，以及其呈現 [**選項**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options)。 這個範例會使用 [**D2D1：： HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper 函數來指定 HWND 和初始大小。 它會使用預設的呈現選項。

第三個參數是接收呈現目標參考之指標的位址。

當您建立轉譯目標並提供硬體加速時，您會在電腦的 GPU 上配置資源。 藉由建立轉譯目標一次並保留最長的時間，您就能獲得效能優勢。 您的應用程式應該建立轉譯目標一次，並在應用程式的存留期內保存它們，或直到收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤為止。 當您收到此錯誤時，您必須重新建立轉譯目標 (以及它所建立) 的任何資源。

## <a name="step-4-create-a-brush"></a>步驟4：建立筆刷

就像 factory 一樣，轉譯目標可以建立繪圖資源。 在此範例中，轉譯目標會建立筆刷。


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



筆刷是繪製區域的物件，例如形狀的筆觸或幾何的填滿。 此範例中的筆刷繪製具有預先定義之純色的區域（黑色）。

Direct2D 也會提供其他類型的筆刷：繪製線性和星形漸層的漸層筆刷，以及用點陣圖和模式繪製的點陣圖筆刷。

某些繪圖 Api 提供畫筆來繪製填滿圖案的外框和筆刷。 Direct2D 不同：它不會提供畫筆物件，而是會使用筆刷繪製外框和填滿圖案。 繪製外框時，請搭配使用 [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) 介面與筆刷來控制路徑的筆劃作業。

筆刷只能搭配建立它的轉譯目標和相同資源網域中的其他轉譯目標使用。 一般情況下，您應該建立筆刷一次，並將其保留在建立它們的呈現目標的存留期內。 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 是獨立的例外狀況;由於建立的成本相對較小，因此您可以在每次繪製框架時建立 **ID2D1SolidColorBrush** ，而不會影響任何明顯的效能。 您也可以使用單一 **ID2D1SolidColorBrush** ，只要在每次使用時都變更其色彩。

## <a name="step-5-draw-the-rectangle"></a>步驟5：繪製矩形

接下來，使用呈現目標來繪製矩形。


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



[**Graphicswindow.drawrectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))方法會採用兩個參數：要繪製的矩形，以及用來繪製矩形外框的筆刷。 （選擇性）您也可以指定 [筆劃寬度]、[虛線模式]、[行聯結] 和 [結束端點] 選項。

您必須在發出任何繪圖命令之前呼叫 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 方法，而且您必須在完成繪製命令之後呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法。 **EndDraw** 方法會傳回 **HRESULT** ，指出繪圖命令是否成功。

## <a name="step-6-release-resources"></a>步驟6：釋放資源

如果沒有更多要繪製的框架，或當您收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤時，請釋放轉譯目標和它所建立的任何裝置。


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



當您的應用程式完成使用 Direct2D 資源 (例如即將結束) 時，請釋放 Direct2D factory。


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a>建立簡單的 Direct2D 應用程式

本主題中的程式碼會顯示 Direct2D 應用程式的基本元素。 為了簡潔起見，此主題省略了應用程式架構和錯誤處理常式代碼，該程式碼是妥善撰寫之應用程式的特性。 如需更詳細的逐步解說，以示範建立簡單 Direct2D 應用程式的完整程式碼，並示範最佳設計做法，請參閱 [建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立簡單的 Direct2D 應用程式](direct2d-quickstart.md)
</dt> </dl>

 

 