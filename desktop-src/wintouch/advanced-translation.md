---
title: Advanced 翻譯
description: Advanced 翻譯
ms.assetid: 48a1bdd5-8b7b-4460-9b7b-1ab8969a28f8
keywords:
- Windows Touch，翻譯
- Windows Touch，advanced 翻譯
- Windows Touch，操作
- 操作，轉譯
- 操作，advanced 翻譯
- translation (轉譯)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc383c71e1f1417d30b64db18aa627039602b942
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839387"
---
# <a name="advanced-translation"></a>Advanced 翻譯

下圖顯示兩個轉譯的解釋。

![圖例會先顯示簡單的轉譯，其中的物件會在沒有旋轉的情況下移動，然後顯示包含移動旋轉的 advanced 平移](images/translation.png)

在範例 A 中，簡單的轉譯範例會移動物件，而不會旋轉。 在 B 範例中，物件會在轉譯期間旋轉，視物件接觸點的位置而定。 如果您啟用單一手指旋轉（如 [單一手指旋轉](single-finger-rotation.md)所述），您可以啟用複雜轉譯。 下圖顯示當您執行轉譯時，單一手指旋轉的各種元件。

![顯示單一手指旋轉元件的圖例： pivotpointx、pivotpointy 和 pivotradius](images/translation-complex-components.png)

移動物件時，會重新計算半徑，並移動軸點。

下列程式碼顯示一種方法，可讓您在啟用複雜轉譯的 [**system.windows.uielement.manipulationdelta>**](/windows/win32/api/manipulations/nf-manipulations-_imanipulationevents-manipulationdelta) 執行時執行此動作。


```C++
    //Apply transformation based on rotationDelta (in radians)
    FLOAT rads = 180.0f / 3.14159f;
    m_dObj->Rotate(rotationDelta*rads, x, y);

    // Apply translation based on scaleDelta
    m_dObj->Scale(scaleDelta);

    // Apply translation based on translationDelta
    m_dObj->Translate(translationDeltaX, translationDeltaY);

    // Set values for one finger rotations
    FLOAT fPivotRadius = (FLOAT)(m_dObj->get_Width() + m_dObj->get_Height())/8.0f;
    FLOAT fPivotPtX = m_dObj->get_CenterX();
    FLOAT fPivotPtY = m_dObj->get_CenterY();
        
    m_manip->put_PivotPointX(fPivotPtX);
    m_manip->put_PivotPointY(fPivotPtY);
    m_manip->put_PivotRadius(fPivotRadius);       
   
```



> [!Note]  
> 物件轉換會在資料透視點和半徑的計算之前發生。 如此一來，如果使用者在移動時對物件執行展開，物件將會正確地移動。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[操作](getting-started-with-manipulations.md)
</dt> </dl>

 

 




