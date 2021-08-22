---
title: 浮凸效果
description: 建立影像的灰階版本，如同已將其加上戳記。
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0fe9b779cbad2b73b877338871f7adff3a36fb4bfb1c291be6de94f736088f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586960"
---
# <a name="emboss-effect"></a>浮凸效果

建立影像的灰階版本，如同已將其加上戳記。

這項效果的 CLSID 是 CLSID \_ D2D1Emboss。

-   [範例影像](#example-image)
-   [範例程式碼](#sample-code)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="example-image"></a>範例影像

![效果輸出的範例](images/emboss-effect.png)

## <a name="sample-code"></a>範例程式碼

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>效果屬性

浮凸效果的屬性是由 [**D2D1 \_ 浮凸 \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) 屬性列舉所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |

## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
