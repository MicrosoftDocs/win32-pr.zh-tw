---
title: 呈現目標、裝置和資源
description: 呈現目標、裝置和資源
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314929"
---
# <a name="render-targets-devices-and-resources"></a>呈現目標、裝置和資源

轉譯 *目標* 只是程式將繪製的位置。 通常，轉譯目標是視窗 (特別是視窗的工作區) 。 它也可以是記憶體中未顯示的點陣圖。 轉譯目標會以 [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) 介面表示。

*裝置* 是一種抽象概念，代表實際繪製圖元的任何內容。 硬體裝置使用 GPU 以加快效能，而軟體裝置則使用 CPU。 應用程式不會建立裝置。 相反地，當應用程式建立轉譯目標時，會隱含地建立裝置。 每個轉譯目標都與特定裝置相關聯，也就是硬體或軟體。

![顯示呈現目標和裝置之間關聯性的圖表。](images/graphics09.png)

*資源* 是程式用來繪製的物件。 以下是 Direct2D 中定義的一些資源範例：

-   **筆刷**。 控制線條和區域的繪製方式。 筆刷類型包含純色筆刷和漸層筆刷。
-   **筆觸樣式**。 控制線條的外觀，例如虛線或純色。
-   **Geometry**。 表示線條和曲線的集合。
-   **網格**。 由三角形組成的圖形。 不同于幾何資料（必須在轉譯之前轉換），GPU 可以直接使用網格資料。

轉譯目標也會被視為一種資源類型。

有些資源會因硬體加速而受益。 此類型的資源一律與特定裝置相關聯，也就是硬體 (GPU) 或軟體 (CPU) 。 這種類型的資源稱為 *裝置相依*。 筆刷和網格是與裝置相關的資源範例。 如果裝置變得無法使用，就必須為新裝置重新建立資源。

無論使用何種裝置，其他資源都會保留在 CPU 記憶體中。 這些資源與 *裝置無關*，因為它們並未與特定裝置建立關聯。 裝置變更時，並不需要重新建立與裝置無關的資源。 筆觸樣式和幾何是與裝置無關的資源。

每個資源的 MSDN 檔會指出資源是與裝置相關或與裝置無關。 每個資源類型都是以衍生自 [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource)的介面表示。 例如，筆刷會以 [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) 介面表示。

## <a name="the-direct2d-factory-object"></a>Direct2D Factory 物件

使用 Direct2D 的第一個步驟是建立 Direct2D factory 物件的實例。 在電腦程式設計中， *factory* 是建立其他物件的物件。 Direct2D factory 會建立下列類型的物件：

-   呈現目標。
-   與裝置無關的資源，例如筆劃樣式和幾何。

裝置依存資源（例如筆刷和點陣圖）是由轉譯目標物件所建立。

![顯示 direct2d factory 的圖表。](images/graphics10.png)

若要建立 Direct2D factory 物件，請呼叫 [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) 函數。


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



第一個參數是指定建立選項的旗標。 **D2D1 \_ FACTORY 型 \_ 別 \_ 單個 \_ 執行緒** 旗標表示您將不會從多個執行緒呼叫 Direct2D。 若要支援來自多個執行緒的呼叫，請指定 **D2D1 \_ FACTORY \_ 類型 \_ 多 \_ 執行緒**。 如果您的程式使用單一執行緒來呼叫 Direct2D，則單一執行緒選項更有效率。

[**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)函數的第二個參數會接收 [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory)介面的指標。

您應該在第一個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息之前建立 Direct2D factory 物件。 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息處理常式是建立 factory 的絕佳位置：


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a>建立 Direct2D 資源

Circle 程式會使用下列與裝置相關的資源：

-   與應用程式視窗相關聯的呈現目標。
-   用來繪製圓形的單色筆刷。

每個資源都是以 COM 介面表示：

-   [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget)介面代表呈現目標。
-   [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush)介面代表筆刷。

Circle 程式會將這些介面的指標儲存為類別的成員變數 `MainWindow` ：


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



下列程式碼會建立這兩個資源。


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



若要建立視窗的呈現目標，請在 Direct2D factory 上呼叫 [**ID2D1Factory：： CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) 方法。

-   第一個參數會指定任何類型之轉譯目標通用的選項。 在這裡，我們會藉由呼叫 helper 函式 [**D2D1：： RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties)來傳遞預設選項。
-   第二個參數指定視窗的控制碼加上轉譯目標的大小（以圖元為單位）。
-   第三個參數會接收 [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) 指標。

若要建立單色筆刷，請在呈現目標上呼叫 [**ID2D1RenderTarget：： CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) 方法。 色彩會以 [**D2D1 \_ 色 \_ F**](/windows/desktop/Direct2D/d2d1-color-f) 值的形式提供。 如需 Direct2D 中色彩的詳細資訊，請參閱 [在 Direct2D 中使用色彩](using-color-in-direct2d.md)。

另請注意，如果轉譯目標已存在，則 `CreateGraphicsResources` 方法會傳回 **\_ [確定]** ，而不執行任何操作。 在下一個主題中，這項設計的原因將會明顯。

## <a name="next"></a>下一個

[使用 Direct2D 繪製](drawing-with-direct2d.md)

 

 