---
title: 如何調整物件
description: 顯示如何調整物件。
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d833ea44e4a38672729dd7647063e8ed9f8de3574d820a3db40d5a848064ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259141"
---
# <a name="how-to-scale-an-object"></a>如何調整物件

本主題說明如何使用 [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) 類別來調整物件。 若要調整物件，表示要讓物件變大或較小。 您可以呼叫下列其中一種方法來調整物件。

-   **Matrix3x2F：： Scale (D2D1 \_ SIZE \_ F SCALEFACTOR，D2D1 \_ POINT \_ 2f centerpoint)**
-   **Matrix3x2F：： Scale (float scalex、float scaley、D2D1 \_ POINT \_ 2f centerpoint)**

第一個方法會將 *scalex* 和 *Scaley* 儲存為 [**D2D1 \_ 大小 \_ F**](/windows/desktop/Direct2D/d2d1-size-f) 結構中的已排序浮點數配對。 第二個方法會將 *scalex* 和 *scaley* 定義為個別參數。

無論您使用哪一種方法，您都必須同時指定 *scalex* 和 *scaley* 因數。 *Scalex* 值是 x 方向的縮放比例。 例如， *scalex* 值1.5 會沿著 X 軸將物件延伸至150%。 同樣地， *scaley* 值是 y 方向的縮放比例。 例如， *scaley* 值0.5 會將物件的高度縮減為 y 軸的50%。

若要將某個點指定為縮放作業的中心點，請使用 *centerpoint* 參數。 根據預設，物件會以其原點為中心 (0、0) 。

下列程式碼範例會建立縮放轉換，以將正方形的大小增加到其原始大小的130%。 *Centerpoint* 會設定為原始正方形的左上角。


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



下圖顯示將刻度轉換套用至正方形的效果。 原始正方形是虛線外框，而縮放的正方形是實心外框。

![正方形的圖已調整大小為130% 的原始大小](images/scale-ovw.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 轉換總覽](direct2d-transforms-overview.md)
</dt> <dt>

[Direct2D 參考](reference.md)
</dt> </dl>

 

 