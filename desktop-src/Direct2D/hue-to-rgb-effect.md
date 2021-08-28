---
title: 色調到 RGB 效果
description: 將 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 影像轉換成 RGB 色彩空間。
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abc45ec09cc77935c332a702648472e6be7edeb06bdf9237e4232f467b1e073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003129"
---
# <a name="hue-to-rgb-effect"></a>色調到 RGB 效果

將 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 影像轉換成 RGB 色彩空間。

HSL 和 HSV 是兩種不同的模型，用來表示圓柱色彩空間中的 RGB 色彩。 這些功能很有用，因為它們可讓您使用更直覺的概念（例如色調和強度），以及結合紅色、綠色和藍色值，來使用色彩的原因。

這種效果會傳遞任何輸入 Alpha 值。

這項效果的 CLSID 是 CLSID \_ D2D1HueToRgb。

若要反轉此效果的行為，請使用 [RGB 到色調效果](rgb-to-hue-effect.md)。

-   [範例程式碼](#sample-code)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="sample-code"></a>範例程式碼

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>效果屬性

對比效果的屬性是由 [**D2D1 \_ HUETORGB \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) 屬性列舉所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 最低支援的伺服器 | Windows 10 \[桌面應用程式 \| Windows 儲存應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |



## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
