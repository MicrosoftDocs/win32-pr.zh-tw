---
title: 對比效果
description: 增加或減少影像的對比。
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025204"
---
# <a name="contrast-effect"></a>對比效果

增加或減少影像的對比。

這項效果的 CLSID 是 CLSID \_ D2D1Contrast。

對比函式會使用兩個分段二 polynomials 來修改每個色頻的值，其會在點 (0.5、0.5) 上符合斜率持續性。

![分段第二次 polynomials 符合斜率持續性， (0.5，0.5) ](images/contrast-effect-slope.png)

-   [範例影像](#example-images)
-   [範例程式碼](#sample-code)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-images"></a>範例影像

此範例會顯示套用最大對比度的效果的輸出 (對比度 = 1.0) 。

之前

![套用效果之前的影像](images/contrast-effect-before.png)

After

![套用效果之後的影像](images/contrast-effect-after.png)

## <a name="sample-code"></a>範例程式碼

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>效果屬性

對比效果的屬性是由 [**D2D1 \_ 對比 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) 屬性列舉所定義。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 最低支援的伺服器 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
