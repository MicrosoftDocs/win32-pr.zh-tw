---
title: 'ID2D1Factory CreateTransformedGeometry 方法 (D2d1 .h) '
description: 轉換指定的幾何，並將結果儲存為 ID2D1TransformedGeometry 物件。
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- CreateTransformedGeometry 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5da3b548c3118209c915714e03fe9e4061c77e96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978629"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>ID2D1Factory：： CreateTransformedGeometry 方法

轉換指定的幾何，並將結果儲存為 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 物件。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                  | 描述                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTransformedGeometry (ID2D1Geometry \* 、D2D \_ 矩陣 \_ 3X2 \_ F \* 、ID2D1TransformedGeometry \* \*)**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | 轉換指定的幾何，並將結果儲存為 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 物件。 <br/> |
| [**CreateTransformedGeometry (ID2D1Geometry \* 、D2D \_ 矩陣 \_ 3X2 \_ F&、ID2D1TransformedGeometry \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | 轉換指定的幾何，並將結果儲存為 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) 物件。 <br/> |



## <a name="remarks"></a>備註

如同其他資源，轉換的幾何會繼承建立它之 factory 的資源空間和執行緒原則。 此物件是不可變的。

使用 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 方法對轉換幾何進行筆劃時，筆劃寬度不會受到套用至幾何的轉換影響。 筆劃寬度只會受到世界轉換的影響。

## <a name="examples"></a>範例

下列範例會建立 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))，然後在不轉換的情況下繪製。 它會產生下圖中顯示的輸出。

![矩形的圖例](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



下一個範例會使用轉譯目標，將幾何調整為3的因數，然後繪製。 下圖顯示在沒有轉換和轉換的情況下繪製矩形的結果;請注意，即使筆觸粗細為1，筆劃在轉換後會變粗。

![具有較粗筆觸的大型矩形內較小矩形的圖例](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



下一個範例會使用 **CreateTransformedGeometry** 方法，將幾何調整為3的因數，然後繪製它。 它會產生下圖中顯示的輸出。 請注意，雖然矩形更大，但其筆觸尚未增加。

![具有相同筆劃的大型矩形內較小矩形的圖例](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
