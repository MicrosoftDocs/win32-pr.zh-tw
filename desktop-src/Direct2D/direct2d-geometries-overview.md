---
title: 幾何概觀
description: 描述 Direct2D 幾何的基本概念、可用於表示、操作及分析圖形的物件。
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D，幾何總覽
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d3f8cd7420325fd876897d538ea9e01a5c0adb64b2d0c55437514773904d6013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825845"
---
# <a name="geometries-overview"></a>幾何概觀

本總覽說明如何建立和使用 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件，以定義和操作2d 圖形。 包含以下幾節。

## <a name="what-is-a-direct2d-geometry"></a>什麼是 Direct2D geometry？

Direct2D geometry 是 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) 物件。 這個物件可以是簡單幾何 ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)、 [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)或 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)) 、路徑幾何 ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) ，或是複合幾何 ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) 和 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)) 。

Direct2D 幾何可讓您描述二維圖形並提供許多用途，例如定義點擊測試區域、裁剪區域，甚至是動畫路徑。

Direct2D 幾何是不可變的，且由 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)建立的裝置獨立資源。 一般而言，您應該建立一次幾何，並將其保留在應用程式的存留期內，或直到必須變更為止。 如需與裝置無關和裝置相依資源的詳細資訊，請參閱 [資源總覽](resources-and-resource-domains.md)。

下列各節說明不同類型的幾何。

## <a name="simple-geometries"></a>簡單幾何

簡單幾何包括 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)、 [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)和 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) 物件，可用來建立基本的幾何圖形，例如矩形、圓角矩形、圓形和省略號。

若要建立簡單幾何，請使用其中一個 [**ID2D1Factory：： create<*GeometryType*>幾何**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 方法。 這些方法會建立指定之類型的物件。 例如，若要建立矩形，請呼叫 [**ID2D1Factory：： CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))，它會傳回 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) 物件;若要建立圓角矩形，請呼叫 [**ID2D1Factory：： CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry))，它會傳回 [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) 物件等等。

下列程式碼範例會呼叫 [**CreateEllipseGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) 方法，並將 *中央* 設定為 (100、100) 、 *x-半徑* 至100，以及 *y 半徑* 至50的橢圓形結構。 然後，它會呼叫 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)，傳入傳回的橢圓形幾何、黑色 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)的指標，以及5的筆觸寬度。 下圖顯示程式碼範例的輸出。

![橢圓形的圖例](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



若要繪製任何幾何的外框，請使用 [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) 方法。 若要繪製其內部，請使用 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法。

## <a name="path-geometries"></a>路徑幾何

路徑幾何會以 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) 介面表示。 這些物件可用來描述由弧線、曲線和線條等線段組成的複雜幾何圖形。 下圖顯示使用路徑幾何建立的繪圖。

![河、山脈和 sun 的圖例](images/path-geo-mnts.png)

如需詳細資訊和範例，請參閱 [路徑幾何總覽](path-geometries-overview.md)。

## <a name="composite-geometries"></a>複合幾何

複合幾何是將幾何分組或與另一個幾何物件合併，或與轉換合併。 複合幾何包含 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) 和 [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) 物件。

### <a name="geometry-groups"></a>Geometry 群組

Geometry 群組是一種方便的方式，可同時將數個幾何分組，讓數個相異幾何的所有圖形都串連成一個。 若要建立 [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup)物件，請在 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件上呼叫 [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup)方法，並在 *fillMode* 中傳入 [**D2D1 \_ 填滿 \_ 模式 \_ 替代**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (替代) 和 **D2D1 \_ 填滿 \_ 模式 \_ 繞組**、要加入至 geometry 群組的幾何物件陣列，以及這個陣列中的元素數目。

下列程式碼範例會先宣告 geometry 物件的陣列。 這些物件是四個具有下列半徑的同心圓：25、50、75和100。 然後，在 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)物件上呼叫 [**CreateGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) ，傳入 [**D2D1 \_ 填滿 \_ 模式 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode)、要加入至 geometry 群組的 geometry 物件陣列，以及這個陣列中的元素數目。


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

下圖顯示從範例呈現兩個群組幾何的結果。

![四個同心圓的圖，其中有一組已填滿的交替環形，另一個則填滿所有環形](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>轉換的幾何

有多種方式可以轉換幾何。 您可以使用轉譯目標的 [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) 方法來轉換轉譯目標繪製的所有專案，或者您可以使用 [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) 方法來建立 [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))，直接將轉換與幾何產生關聯。

您應該使用的方法取決於您想要的效果。 當您使用轉譯目標來轉換幾何，然後轉譯幾何時，轉換會影響幾何的所有內容，包括您已套用的任何筆觸寬度。 另一方面，當您使用 [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)時，轉換只會影響描述圖形的座標。 繪製幾何時，轉換不會影響筆觸粗細。

> [!Note]  
> 從 Windows 8 開始，世界轉換並不會影響筆觸粗細的筆觸粗細 [**D2D1 \_ 筆觸 \_ 轉換 \_ 類型 \_ 固定**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)或 [**D2D1 \_ 筆觸 \_ 轉換 \_ 類型 \_**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)的最細效果。 您應使用這些轉換類型來達成轉換的獨立筆劃

 

下列範例會建立 [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)，然後在不轉換的情況下繪製。 它會產生下圖中顯示的輸出。

![矩形的圖例](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



下一個範例會使用轉譯目標，將幾何調整為3的因數，然後繪製。 下圖顯示在沒有轉換和轉換的情況下繪製矩形的結果。 請注意，即使筆觸粗細為1，筆劃在轉換後會變寬。

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



下一個範例會使用 [**CreateTransformedGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) 方法，將幾何調整為3的因數，然後繪製它。 它會產生下圖中顯示的輸出。 請注意，雖然矩形更大，但其筆觸尚未增加。

![具有相同筆觸粗細之大型矩形內較小矩形的圖例](images/transformedgeometry2-step3.png)


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
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a>以遮罩形式的幾何

當您呼叫 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))方法時，您可以使用 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)物件做為幾何遮罩。 幾何遮罩會指定複合到轉譯目標的圖層區域。 如需詳細資訊，請參閱 [圖層](direct2d-layers-overview.md)的 [幾何遮罩] 區段。

## <a name="geometric-operations"></a>幾何作業

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)介面提供數個幾何運算，可讓您用來操作和測量幾何圖形。 例如，您可以使用它們來計算並傳回其界限、比較，以瞭解一個幾何如何在空間上與另一個幾何相關聯 (適用于點擊測試) 、計算區域和長度等等。 下表說明常見的幾何作業。



| 作業                                                   | 方法                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 合併                                                     | [**CombineWithGeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| 界限/加寬界限/抓取界限、變更區域更新 | [**加寬**](id2d1geometry-widen.md)、 [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds)、 [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)                             |
| 點擊測試                                                 | [**FillContainsPoint**](id2d1geometry-fillcontainspoint.md)、 [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                             |
| 筆勢                                                      | [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| 比較                                                  | [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| 簡化 (移除弧形和二次方貝茲曲線)    | [**簡化**](id2d1geometry-simplify.md)                                                                                                                                 |
| 鑲嵌                                                | [**Tessellate**](id2d1geometry-tessellate.md)                                                                                                                             |
|  (移除交集) 外框                               | [**外框**](id2d1geometry-outline.md)                                                                                                                                   |
| 計算幾何的區域或長度                  | [**ComputeArea**](id2d1geometry-computearea.md)、 [**ComputeLength**](id2d1geometry-computelength.md)、 [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> 從 Windows 8 開始，您可以在 [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1)上使用 [**ComputePointAndSegmentAtLength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description))方法來計算幾何的區域或長度。

 

### <a name="combining-geometries"></a>結合幾何

若要將一個幾何與另一個幾何結合，請呼叫 [**ID2D1Geometry：： CombineWithGeometry**](id2d1geometry-combinewithgeometry.md) 方法。 當您合併幾何時，可以指定下列四種方式之一來執行合併作業： [**D2D1 合併模式聯 \_ \_ \_ 集**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (聯集) 、 [**D2D1 \_ 合併 \_ 模式 \_ 交集**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (交集) 、 [**D2D1 \_ 合併 \_ 模式 \_ XOR**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (xor) ，以及 [**D2D1 \_ 合併 \_ 模式 \_ 排除**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (排除) 。 下列程式碼範例會示範兩個使用聯集合並模式結合的圓形，其中第一個圓形的中心點是 (75、75) 和半徑50的半徑，而第二個圓圈具有 (125、75) 和50半徑的中心點。


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



下圖顯示結合了 union 模式的兩個圓形。

![將兩個重迭的圓形合併為聯集的圖例](images/combine-mode-union.png)

如需所有合併模式的圖例，請參閱 [**D2D1 \_ 合併 \_ 模式列舉**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode)。

### <a name="widen"></a>擴大

[**擴大**](id2d1geometry-widen.md)方法會產生新的幾何，其填滿相當於對現有幾何進行筆劃，然後將結果寫入至指定的 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)物件。 下列程式碼範例會呼叫 [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)物件上的 [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) 。 如果 **開啟** 成功，它會對 geometry 物件呼叫 **加寬** 。


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a>Tessellate

[**Tessellate**](id2d1geometry-tessellate.md)方法會建立一組順向纏繞三角形，以在使用指定的矩陣進行轉換之後，以指定的誤差來轉換幾何。 下列程式碼範例會使用 **Tessellate** 來建立代表 *pPathGeometry* 的三角形清單。 三角形會儲存在 [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)、 *pMesh*，然後傳送至類別成員 *m \_ pStrokeMesh*，以供稍後轉譯時使用。


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a>FillContainsPoint 和 StrokeContainsPoint

[**FillContainsPoint**](id2d1geometry-fillcontainspoint.md)方法會指出幾何所填滿的區域是否包含指定的點。 您可以使用這個方法來進行點擊測試。 下列程式碼範例會在 [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)物件上呼叫 **FillContainsPoint** ，並在 (0、0) 和身分 [**識別**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity)矩陣的點傳入點。


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



[**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)方法會判斷幾何的筆劃是否包含指定的點。 您可以使用這個方法來進行點擊測試。 下列程式碼範例會使用 **StrokeContainsPoint**。


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a>簡化 

[**簡化**](id2d1geometry-simplify.md)方法會從指定的幾何中移除弧形和二次方貝茲曲線。 因此，產生的幾何只會包含線條和（選擇性）三次方貝茲曲線。 下列程式碼範例使用 **簡化** ，將具有貝茲曲線的幾何轉換成隻包含線段的幾何。


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a>ComputeLength 和 ComputeArea

如果每個區段都展開成一行， [**ComputeLength**](id2d1geometry-computelength.md) 方法就會計算指定之幾何的長度。 這包括當幾何關閉時的隱含結尾區段。 下列程式碼範例會使用 **ComputeLength** 來計算指定之圓形 (**m \_ pCircleGeometry1**) 的長度。


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



[**ComputeArea**](id2d1geometry-computearea.md)方法會計算指定幾何的區域。 下列程式碼範例會使用 **ComputeArea** 來計算指定之圓形的區域 (**m \_ pCircleGeometry1**) 。


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>CompareWithGeometry

[**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)方法會描述呼叫這個方法的幾何和指定幾何之間的交集。 交集的可能值包括 [**D2D1 \_ 幾何 \_ 關聯 \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) 性 (不連續的) 、 **D2D1 GEOMETRY (\_ \_ 關聯 \_ \_** 包含) 、 **D2D1 \_ geometry \_ 關聯 \_ 包含** (包含) ，以及 **D2D1 \_ 幾何 \_ 關聯 \_** (重迭) 重迭。 「無交集」表示兩個幾何填滿完全不相交。 「包含」表示幾何完全由指定的幾何所包含。 「contains」表示幾何完全包含指定的幾何，而「重迭」表示兩個幾何重迭，但不完全包含另一個。

下列程式碼範例顯示如何比較兩個半徑為50但位移為50的圓形。


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a>外框

[ [**外框**](id2d1geometry-outline.md) ] 方法會計算幾何的輪廓 (某個幾何的版本，其中沒有任何圖與本身或任何其他圖表) ，並將結果寫入至 [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink)。 下列程式碼範例使用 **大綱** 來建立不具任何自我交集的相等幾何。 它會使用預設的簡維容錯。


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a>GetBounds 和 GetWidenedBounds

[**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds)方法會捕獲幾何的界限。 下列程式碼範例會使用 **GetBounds** 來取出指定之圓形 (**m \_ pCircleGeometry1**) 的界限。


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



[**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)方法會在指定的筆觸寬度和樣式（由指定的矩陣轉換）加寬之後，抓取幾何的範圍。 下列程式碼範例會使用 **GetWidenedBounds** 來抓取指定之圓形的範圍 (**m \_ pCircleGeometry1**) 在以指定的筆觸寬度加寬之後。


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a>ComputePointAtLength

[**ComputePointAtLength**](id2d1geometry-computepointatlength.md)方法會在幾何的指定距離計算點和正切向量。 下列程式碼範例會使用 **ComputePointAtLength**。


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[路徑幾何總覽](path-geometries-overview.md)
</dt> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 