---
title: 'ID2D1RenderTarget PushLayer 方法 (D2d1 \_ 1 .h) '
description: 將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 PopLayer 為止。
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- PushLayer 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979604"
---
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget：:P ushLayer 方法

將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 為止。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                            | 描述                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PushLayer (D2D1 \_ 層 \_ 參數&、ID2D1Layer \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | 將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 為止。 <br/> |
| [**PushLayer (D2D1 \_ 層 \_ 參數 \* ，ID2D1Layer \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | 將指定的圖層新增至轉譯目標，使其接收所有後續的繪圖作業，直到呼叫 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 為止。 <br/> |



## <a name="remarks"></a>備註

[**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))方法可讓呼叫端開始將轉譯重新導向至圖層。 所有轉譯作業在圖層中都是有效的。 圖層的位置會受到轉譯目標上設定的世界轉換影響。

每個 **PushLayer** 都必須有相符的 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) 呼叫。 如果有比 **PushLayer** 呼叫更多的 **PopLayer** 呼叫，轉譯目標會置於錯誤狀態。 如果在所有未處理的層上取出之前呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) ，轉譯目標會進入錯誤狀態，而且會傳回錯誤。 您可以呼叫 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)來清除錯誤狀態。

特定的 [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) 資源只能一次作用。 換句話說，您無法呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) 方法，然後緊接在另一個具有相同圖層資源的 **PushLayer** 方法之後。 相反地，您必須使用不同的層級資源來呼叫第二個 **PushLayer** 方法。

如需範例，請參閱 [如何裁剪具有圖層的區域](how-to-clip-with-layers.md)。

如果失敗，這個方法不會傳回錯誤碼。 若要判斷繪圖作業 (如 **PushLayer**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。

## <a name="examples"></a>範例

下列範例會使用圖層，將點陣圖裁剪成幾何遮罩。 如需完整的範例，請參閱 [如何裁剪成幾何遮罩](how-to-clip-with-layers.md)。


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

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

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1 \_ 1. h (包括 D2d1) </dt> </dl> |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[圖層總覽](direct2d-layers-overview.md)
</dt> </dl>

�

�
