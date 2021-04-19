---
title: 'ID2D1GeometrySink AddBezier 方法 (D2d1 .h) '
description: 在目前的點和指定的結束點之間建立三次方貝茲曲線，然後將它新增至幾何接收器。
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- AddBezier 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b470129350463920583c34bec5f886f60b16485e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978787"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a>ID2D1GeometrySink：： AddBezier 方法

在目前的點和指定的結束點之間建立三次方貝茲曲線，然後將它新增至幾何接收器。

### <a name="overload-list"></a>多載清單



| 方法                                                                                            | 描述                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**AddBezier (D2D1 \_ 貝塞爾 \_ 區段&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))  | 在目前的點和指定的結束點之間建立三次方貝茲曲線。<br/> |
| [**AddBezier (D2D1 \_ 貝塞爾 \_ 區段 \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment)) | 在目前的點和指定的結束點之間建立三次方貝茲曲線。<br/>  |



## <a name="examples"></a>範例

下列範例會建立 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)、抓取接收器，並用它來定義沙漏圖形。 如需完整的範例，請參閱 [如何繪製和填滿複雜的圖形](how-to-draw-and-fill-a-complex-shape.md)。


```C++
ID2D1GeometrySink *pSink = NULL;



// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
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
        SafeRelease(&pSink);
    }
}
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

�

�
