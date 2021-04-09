---
title: 如何扭曲物件
description: 顯示如何扭曲物件。
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842599"
---
# <a name="how-to-skew-an-object"></a>如何扭曲物件

若要扭曲 (或切變) 物件表示要從 X 軸、y 軸或兩者的指定角度扭曲物件。 例如，當您扭曲正方形時，它會變成平行四邊形。

[**Matrix3x2F：：扭曲**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)方法會使用3個參數：

-   *system.windows.media.skewtransform.anglex*： X 軸扭曲角度，以從 y 軸逆時針算起的度數來測量。
-   *system.windows.media.skewtransform.angley*： y 軸扭曲角度（以度為單位，從 X 軸順時針測量）。
-   *centerPoint*：扭曲的執行點。

若要預測扭曲轉換的效果，請考慮 *system.windows.media.skewtransform.anglex* 是從 y 軸逆時針算起的扭曲角度（以度為單位）。 例如，如果 *system.windows.media.skewtransform.anglex* 設定為30，則物件會沿著 y 軸逆時針旋轉30度的 *centerPoint*。 下圖顯示正方形左上角的垂直扭曲30度。

![從 y 軸逆時針算起30度的正方形圖例](images/skewx.png)

同樣地， *system.windows.media.skewtransform.angley* 是以度為單位，從 X 軸順時針測量的扭曲角度。 例如，如果 *system.windows.media.skewtransform.angley* 設定為30，則物件會沿著 X 軸順時針扭曲 *centerPoint* 的30度。 下圖顯示正方形左上角的垂直扭曲30度。

![從 X 軸順時針扭曲30度的正方形圖例](images/skewy.png)

如果您將 *system.windows.media.skewtransform.anglex* 和 *system.windows.media.skewtransform.angley* 設定為30度，並將 *centerPoint* 設定為正方形的左上角，您將會看到下列扭曲方形 (實心的) 。 請注意，扭曲的正方形會從 y 軸逆時針算起，從 X 軸順時針算起的30度扭曲。

![從 y 軸逆時針算起，從 X 軸順時針算30度的正方形圖](images/skewxy.png)

下列程式碼範例會水準誤差正方形左上角的正方形45度數。


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



下圖顯示將扭曲轉換套用至正方形的效果，其中原始正方形是虛線輪廓，而扭曲的物件 (平行四邊形) 是實心外框。 請注意，傾斜角度的誤差是從 y 軸逆時針算算的45度。

![從 y 軸逆時針扭曲45度的正方形圖例](images/skew-ovw.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 轉換總覽](direct2d-transforms-overview.md)
</dt> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 