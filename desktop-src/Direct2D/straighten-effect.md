---
title: 伸直效果
description: 旋轉並選擇性地調整影像。
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d777859fa35dc3dafc3507586e76309049fa170e42bb29f4b214cc704fd24c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664958"
---
# <a name="straighten-effect"></a>伸直效果

旋轉並選擇性地調整影像。

這項效果的 CLSID 是 CLSID \_ D2D1Straighten。

-   [範例影像](#example-image)
-   [範例程式碼](#sample-code)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

![效果輸出的範例](images/straighten-effect.png)

## <a name="sample-code"></a>範例程式碼


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>效果屬性

伸直效果的屬性是由 [**D2D1 的 \_ 伸直 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) 屬性列舉所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |


## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

