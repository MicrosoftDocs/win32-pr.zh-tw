---
title: 如何裁剪成幾何遮罩
description: 顯示如何使用圖層來裁剪區域。
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c2258938020593014b5b6f5ea77516e7770f8589601cf4139971b3532b22fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569341"
---
# <a name="how-to-clip-to-a-geometric-mask"></a>如何裁剪成幾何遮罩

本主題說明如何使用幾何遮罩來裁剪圖層的區域。

**使用幾何遮罩來裁剪區域**

1.  建立將用來裁剪區域的 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 。
2.  呼叫 [**ID2D1RenderTarget：： CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 來建立圖層。
3.  呼叫 [**ID2D1RenderTarget：:P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 並傳遞您在步驟1中定義的幾何遮罩。
4.  將內容繪製至剪輯。
5.  呼叫 [**ID2D1RenderTarget：:P oplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) ，將圖層從呈現目標中移除。

接下來的範例會使用幾何遮罩來裁剪影像和數個矩形。 下圖顯示左邊的原始點陣圖，以及裁剪至右側幾何遮罩的點陣圖。

![點陣圖裁剪成星形遮罩之前和之後的金魚點陣圖圖例](images/cliparegion-layers.png)

若要裁剪繪圖（如上圖所示），您可以建立一個 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) ，並用它來定義星形。 下列程式碼示範如何執行這項操作。


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) 來建立圖層。

> [!Note]  
> 從 Windows 8 開始，您不需要呼叫 [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))。 在大部分情況下，如果您未呼叫此方法，而 Direct2D 管理層資源，則效能會比較好。

 

使用幾何遮罩呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 來推送圖層。 將內容繪製到剪輯，然後呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 以彈出圖層。 這會產生星形繪圖。 下列程式碼示範如何執行這項操作。


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[圖層總覽](direct2d-layers-overview.md)
</dt> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 