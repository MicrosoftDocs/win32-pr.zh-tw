---
title: 如何轉譯物件
description: 顯示如何轉譯物件。
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316087"
---
# <a name="how-to-translate-an-object"></a>如何轉譯物件

若要轉譯2D 物件，請沿著 X 軸、y 軸或兩者移動物件。 您可以呼叫下列其中一種方法來建立轉譯轉換。

-   [**轉譯 (D2D1 \_大小： \_ F 大小)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))：採用已排序的配對，定義沿著 X 軸和 y 軸平移的距離。
-   [**轉譯 (float x，float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float))：採用沿著 X 軸平移的距離，以及沿著 y 軸平移的距離。

下列程式碼會建立轉譯轉換矩陣，沿著 X 軸將正方形20單位向右移動，沿著 y 軸向下移動10個單位。


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



下圖顯示將轉譯轉換套用至正方形的效果，其中原始正方形是虛線外框，而轉譯的正方形是實心外框。

![正方形的圖例將沿著 X 軸向右移動20個單位，並沿著 y 軸向下移動10個單位](images/translation-ovw.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct2D 參考](reference.md)
</dt> <dt>

[Direct2D 轉換總覽](direct2d-transforms-overview.md)
</dt> </dl>

 

 