---
title: 使用 Direct2D 繪製
description: 建立圖形資源之後，您就可以開始繪製。
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d8a346300b32fe1c716e51efe6bfb8fdbf6220fb2ff17df6de617de27ba1a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535071"
---
# <a name="drawing-with-direct2d"></a>使用 Direct2D 繪製

建立圖形資源之後，您就可以開始繪製。

## <a name="drawing-an-ellipse"></a>繪製橢圓形

[Circle](your-first-direct2d-program.md)程式會執行非常簡單的繪圖邏輯：

1.  以純色填滿背景。
2.  繪製實心的圓形。

![圓形程式的螢幕擷取畫面。](images/graphics08.png)

由於轉譯目標是視窗 (而不是點陣圖或其他螢幕外表面) ，因此繪圖是為了回應 [**WM \_ 繪製**](/windows/desktop/gdi/wm-paint) 訊息而完成。 下列程式碼顯示圓形程式的視窗程式。


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

以下是繪製圓形的程式碼。

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



[**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget)介面用於所有繪製作業。 程式的 `OnPaint` 方法會執行下列動作：

1.  [**ID2D1RenderTarget：： BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)方法表示繪圖的起點。
2.  [**ID2D1RenderTarget：： Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)方法會以純色填滿整個呈現目標。 色彩會以 [**D2D1 \_ 色 \_ F**](/windows/desktop/Direct2D/d2d1-color-f) 結構的形式提供。 您可以使用 [**D2D1：： ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) 類別來初始化結構。 如需詳細資訊，請參閱 [在 Direct2D 中使用色彩](using-color-in-direct2d.md)。
3.  [**ID2D1RenderTarget：： FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))方法會繪製填滿的橢圓形，並使用指定的筆刷來填滿。 橢圓形是由中心點以及 x 和 y 半徑來指定。 如果 x 和 y 半徑相同，則結果為圓形。
4.  [**ID2D1RenderTarget：： EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)方法會針對此框架完成繪圖的信號。 所有繪圖作業都必須放在對 [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) 和 **EndDraw** 的呼叫之間。

[**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)、 [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)和 [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))方法都有 **void** 傳回型別。 如果在這些方法的任何一執行期間發生錯誤，則會透過 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 方法的傳回值發出錯誤。 `CreateGraphicsResources`方法會顯示在[建立 Direct2D 資源](render-targets--devices--and-resources.md)的主題中。 這個方法會建立呈現目標和純色筆刷。

裝置可能會緩衝繪製命令並順延強制，直到呼叫 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 為止。 您可以藉由呼叫 [**ID2D1RenderTarget：： Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush)來強制裝置執行任何暫止的繪圖命令。 不過，清除可能會降低效能。

## <a name="handling-device-loss"></a>處理裝置遺失

當程式正在執行時，您所使用的圖形裝置可能會變成無法使用。 例如，如果顯示解析度變更，或使用者移除顯示器介面卡，則裝置可能會遺失。 如果裝置遺失，轉譯目標也會變成無效，以及與裝置相關聯之任何裝置相依的資源。 Direct2D 藉由從 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)方法傳回錯誤碼 **D2DERR 重新建立 \_ \_ 目標**，來為遺失的裝置發出信號。 如果您收到此錯誤碼，則必須重新建立轉譯目標和所有裝置相依的資源。

若要捨棄資源，只要釋放該資源的介面即可。


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



建立資源可能是昂貴的作業，因此請勿重新建立每個 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息的資源。 建立資源一次，並快取資源指標，直到資源因為裝置遺失而變成無效，或直到您不再需要該資源為止。

## <a name="the-direct2d-render-loop"></a>Direct2D 轉譯迴圈

無論您的繪圖為何，您的程式都應該執行如下所示的迴圈。

1.  建立與裝置無關的資源。
2.  呈現場景。
    1.  檢查有效的轉譯目標是否存在。 如果沒有，請建立轉譯目標和裝置相依的資源。
    2.  呼叫 [**ID2D1RenderTarget：： BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)。
    3.  發出繪製命令。
    4.  呼叫 [**ID2D1RenderTarget：： EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)。
    5.  如果 [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 傳回 **D2DERR \_ 重新建立 \_ 目標**，請捨棄轉譯目標和裝置相依的資源。
3.  每當您需要更新或重繪場景時，重複步驟2。

如果呈現目標為視窗，則每當視窗收到 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息時，就會發生步驟2。

此處所顯示的迴圈會捨棄裝置相依的資源，並在下一個迴圈開始時重新建立， (步驟 2a) 來處理裝置遺失。

## <a name="next"></a>下一個

[DPI 和 Device-Independent 圖元](dpi-and-device-independent-pixels.md)

 

 