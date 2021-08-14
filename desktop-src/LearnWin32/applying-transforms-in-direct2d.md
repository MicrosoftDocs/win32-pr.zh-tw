---
title: 在 Direct2D 中套用轉換
description: 在 Direct2D 中套用轉換
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83cb9a7981ada944de07e362c2f568889a84a4f90f2171150fbab948ab3a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388483"
---
# <a name="applying-transforms-in-direct2d"></a>在 Direct2D 中套用轉換

在 [使用 Direct2D 繪圖](drawing-with-direct2d.md)時，我們看到 [**ID2D1RenderTarget：： FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) 方法繪製了一個對齊 X 軸和 y 軸的橢圓形。 但是，假設您想要以角度來繪製橢圓形？

![顯示傾斜橢圓形的影像。](images/graphics16.png)

藉由使用轉換，您可以透過下列方式更改圖形。

-   圍繞點旋轉。
-   縮放。
-   ) X 或 Y 方向的轉譯 (位移。
-   扭曲 (也稱為 *切變*) 。

轉換是將一組點對應到一組新點的數學運算。 例如，下圖顯示圍繞點 P3 旋轉的三角形。 套用旋轉之後，點 P1 會對應到 P1 '，點 P2 會對應到 P2 '，而 point P3 會對應到本身。

![顯示圍繞點旋轉的圖表。](images/graphics17.png)

轉換是使用矩陣來執行的。 不過，您不需要瞭解矩陣的數學運算就能使用。 如果您想要深入瞭解數學，請參閱 [附錄：矩陣轉換](appendix--matrix-transforms.md)。

若要在 Direct2D 中套用轉換，請呼叫 [**ID2D1RenderTarget：： SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) 方法。 這個方法會採用 [**D2D1 \_ 矩陣 \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) 結構來定義轉換。 您可以藉由呼叫 [**D2D1：： Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別上的方法來初始化此結構。 這個類別包含的靜態方法會傳回每一種轉換的矩陣：

-   [**Matrix3x2F：：輪替**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F：： Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F：：轉譯**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F：：扭曲**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

例如，下列程式碼會在 (100，100) 的點周圍套用20度的旋轉。


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

轉換會套用至所有後續的繪圖操作，直到您再次呼叫 [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) 為止。 若要移除目前的轉換，請使用身分識別矩陣來呼叫 **SetTransform** 。 若要建立身分識別矩陣，請呼叫 [**Matrix3x2F：： identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) 函數。


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>繪製時鐘手

讓我們將圓形程式轉換成類比時鐘來放置轉換。 我們可以藉由新增手線來完成這項作業。

![類比時鐘程式的螢幕擷取畫面。](images/graphics18.png)

我們可以計算角度，然後套用旋轉轉換，而不是計算線條的座標。 下列程式碼顯示一個可繪製一次時鐘的函式。 *FAngle* 參數提供手的角度（以度為單位）。

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

這段程式碼會繪製一條垂直線，從時鐘面的中央開始，然後結束于點 *端點*。 線條是藉由套用旋轉轉換，在橢圓形的中央周圍旋轉。 旋轉的中心點是形成時鐘面的橢圓形中心。

![顯示時鐘手旋轉的圖表。](images/graphics19.png)

下列程式碼顯示如何繪製整個時鐘臉部。

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

您可以從[Direct2D Clock 範例](direct2d-clock-sample.md)下載完整的 Visual Studio 專案。  (只是為了有趣，下載版本會將放射星形 gradiant 新增至時鐘臉部。 ) 

## <a name="combining-transforms"></a>合併轉換

四個基本轉換可以藉由將兩個以上的矩陣相乘來合併。 例如，下列程式碼會結合旋轉與轉譯。

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

[**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f)類別提供矩陣乘法的 [**運算子 \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) 。 您將矩陣相乘的順序很重要。 設定轉換 (M x N) 表示「先套用 M，後面接著 N」。 例如，以下是旋轉，後面接著平移：

![顯示旋轉後接平移的圖表。](images/graphics20.png)

以下是此轉換的程式碼：

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

現在將該轉換與反向順序中的轉換進行比較，並在後面接著旋轉。

![顯示轉譯後接旋轉的圖表。](images/graphics21.png)

旋轉是在原始矩形的中央周圍執行。 以下是此轉換的程式碼。

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

如您所見，矩陣是相同的，但作業的順序已變更。 發生這種情況是因為矩陣乘法不是可交換的： M x N ≠ N x M。

## <a name="next"></a>下一個

[附錄：矩陣轉換](appendix--matrix-transforms.md)