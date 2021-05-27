---
title: 'ID2D1RenderTarget CreateGradientStopCollection 方法 (D2d1 \_ 1 .h) '
description: 從 D2D1 梯度停用結構的指定陣列建立 ID2D1GradientStopCollection \_ \_ 。
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- CreateGradientStopCollection 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: f099c1c71015ca433299843d388085103571d31d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549413"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a>ID2D1RenderTarget：： CreateGradientStopCollection 方法

從 [**D2D1 \_ 梯度 \_ 停**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)用結構的指定陣列建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                                                               | 描述                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateGradientStopCollection (D2D1 \_ 梯度 \_ 停駐 \* 、D2D1 \_ GAMMA、D2D1 \_ 擴充 \_ 模式、ID2D1GradientStopCollection \* \*)**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) | 從指定的漸層停駐點、色彩插補 gamma 和延伸模式建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 。 <br/>                                                              |
| [**CreateGradientStopCollection (D2D1 \_ 梯度 \_ 停駐 \* 、ID2D1GradientStopCollection \* \*)**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)                                                            | 從指定的漸層停用 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) ，使用 [**D2D1 \_ GAMMA \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) 色彩插補 GAMMA 和 [夾具延伸模式] 來建立。<br/> |



## <a name="examples"></a>範例

下列範例會建立梯度停駐點的陣列，然後使用它們來建立 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)。


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



下一個程式碼範例會使用 [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) 來建立 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)。


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
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

[**D2D1 \_ 梯度 \_ 停駐點**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[如何建立線性漸層筆刷](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[如何建立放射狀漸層筆刷](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[筆刷概觀](direct2d-brushes-overview.md)
</dt> </dl>