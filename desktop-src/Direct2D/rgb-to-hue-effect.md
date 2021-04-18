---
title: RGB 到色調效果
description: 將 RGB 影像轉換成 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 色彩空間。
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384490"
---
# <a name="rgb-to-hue-effect"></a>RGB 到色調效果

將 RGB 影像轉換成 HSL (色調、飽和度、亮度) 或 HSV (色調、飽和度、值) 色彩空間。

HSL 和 HSV 是兩種不同的模型，用來表示圓柱色彩空間中的 RGB 色彩。 這些功能很有用，因為它們可讓您使用更直覺的概念（例如色調和強度），以及結合紅色、綠色和藍色值，來使用色彩的原因。

此效果會將輸出資料正規化 (的色調、HSV 或色調的飽和度值、在 HSL) 的飽和度、亮度、範圍 \[ 0、1 \] 。

這項效果的 CLSID 是 CLSID \_ D2D1RgbToHue。

若要反轉此效果的行為，請使用 [色調到 RGB 效果](hue-to-rgb-effect.md)。

-   [範例程式碼](#sample-code)
-   [效果屬性](#effect-properties)
-   [需求](#requirements)
-   [相關主題](#related-topics)

## <a name="sample-code"></a>範例程式碼


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a>效果屬性

對比效果的屬性是由 [**D2D1 \_ RGBTOHUE \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) 屬性列舉所定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------|
| 最低支援的用戶端 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 最低支援的伺服器 | Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\] |
| 標頭                   | d2d1effects \_ 2。h                                  |
| 程式庫                  | d2d1 .lib，dxguid .lib                              |


## <a name="related-topics"></a>相關主題

* [ID2D1Effect 介面](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
