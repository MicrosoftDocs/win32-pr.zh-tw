---
title: 'ID2D1Brush SetTransform 方法 (D2d1 \_ 1 .h) '
description: 設定套用至筆刷的轉換。
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- SetTransform 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997036"
---
# <a name="id2d1brushsettransform-methods"></a>ID2D1Brush：： SetTransform 方法

設定套用至筆刷的轉換。

### <a name="overload-list"></a>多載清單



| 方法                                                                                       | 描述                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | 設定套用至筆刷的轉換。<br/> |
| [**SetTransform (D2D1 \_ 矩陣 \_ 3X2 \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | 設定套用至筆刷的轉換。<br/> |



## <a name="remarks"></a>備註

當您使用筆刷繪製時，它會在呈現目標的座標空間中繪製。 筆刷不會自動自行定位，以配合正在繪製的物件;根據預設，它們會在呈現目標的原點 (0、0) 開始繪製。

您可以藉由設定起點和終點，將 [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) 所定義的漸層「移動」至目的地區域。 同樣地，您可以藉由變更中央和半徑來移動 [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) 所定義的漸層。

若要將 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的內容對齊正在繪製的區域，您可以使用 **SetTransform** 方法將點陣圖轉譯為所需的位置。 此轉換只會影響筆刷;它不會影響呈現目標所繪製的任何其他內容。

下圖顯示使用 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 填滿位於 (100，100) 之矩形的效果。 左圖上的圖例顯示填滿矩形的結果，而不會轉換筆刷：點陣圖是在轉譯目標的原點繪製。 如此一來，矩形中只會出現點陣圖的一部分。

右邊的圖例顯示轉換 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) 的結果，使其內容會向右移動50圖元，並向下移動50圖元。 點陣圖現在會填滿矩形。

![兩個方塊的圖例，其中一個是以沒有已轉換筆刷的點陣圖繪製，另一個則使用已轉換的筆刷繪製](images/brushes-ovw-transform.png)

## <a name="examples"></a>範例

下列程式碼範例示範如何建立在上圖中右圖所示的轉換。 首先，將翻譯套用至 [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)，並沿著 y 軸沿著 X 軸和50圖元向下移動筆刷50圖元。 然後使用 **ID2D1BitmapBrush** 來填滿左上角的矩形，其位於 (100、100) ，而右下角的 (200，200) 。


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1 \_ 1. h (包括 D2d1) </dt> </dl> |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[筆刷概觀](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
