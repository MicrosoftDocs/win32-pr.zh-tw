---
title: 自訂功能區色彩
description: Windows 功能區架構會公開一組色彩屬性，讓應用程式在執行時間自訂各種功能區 UI 元素的外觀。
ms.assetid: e070aaca-d350-4336-8e5d-d5d9c8167287
keywords:
- Windows功能區、自訂色彩
- 功能區、自訂色彩
- 自訂 Windows 功能區色彩
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ef83c40d49656c82aabfbf41c4ec5375f7f3f54f063ccf30d917e740f87408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710888"
---
# <a name="customizing-ribbon-colors"></a>自訂功能區色彩

Windows 功能區架構會公開一組色彩屬性，讓應用程式在執行時間自訂各種功能區 UI 元素的外觀。

-   [簡介](#introduction)
-   [指定功能區色彩](#specify-ribbon-colors)
-   [將 RGB 轉換成 HSB](#convert-rgb-to-hsb)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

下表所列的 [framework 屬性索引鍵](windowsribbon-reference-properties-framework.md) 可用來設定功能區應用程式中各種 UI 元素的色彩。 這些屬性可讓功能區架構支援跨應用程式的個人化、身分識別需求和商標規格。

| 功能區色彩                     | Framework 屬性索引鍵                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 背景色彩                 | [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)                                                                                                                                                                                                                                                                                                                                                                 |
| 醒目提示色彩 (僅 Windows 7)  | [UI \_Windows 8 \_ ](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)* *： * * [ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)中引進的 PKEY GlobalHighlightColor * * * 無法獨立于[ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)之外進行設定。<br/> <br/>                                                              |
| 文字色彩                       | [UI \_PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)* * * * 在 Windows 8 引進 **：** Windows 8 中 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)的預設值變更，可能需要在針對 Windows 7 設計的功能區應用程式中調整 [ui \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) 。<br/> <br/> |



 

## <a name="specify-ribbon-colors"></a>指定功能區色彩

功能區架構會使用色調、飽和度、亮度 (HSB) 色彩模型，其不同于較常見的色調、飽和度、亮度 (HSL) 或色調、飽和度、值 (HSV) 色彩空間。 尤其是 B 代表整體的亮度或亮度層級，而不是特定色彩的亮度。

若要在功能區架構中指定 UI 元素的色彩，應用程式會將 HSB 值指派給每個全域色彩屬性。 然後，這些值會在功能區應用程式所需的所有功能區專案中通用套用 (架構不支援將 HSB 值指派給個別元素和控制項) 。

在 Windows 8 * *： * *[ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)中引進，指派的值與[ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)相同。

下表描述功能區架構 HSB 參數。



元件

描述

調整的值\*

色調 (H) 

Pigment （或實際的色彩）通常會識別為介於0到359度的 circlular 範圍內的值。

0 (紅色) 至 255 (紅色) 

飽和度 (S) 

以百分比表示的色彩的純度或飽和度，從0到100%。

0 (灰色) 255 (完全飽和) 

亮度 (B) 

色彩的整體亮度或暗度，以從0到100% 的百分比表示。

0 (深色) 至 255 (light) 

\* 針對架構，每個參數值的原始範圍會轉譯為0到255的範圍。



 

HSB 值不會識別特定的色彩。 相反地，HSB 屬性值的組合會影響整個 UI 中色彩漸層的色彩漸層相對於彼此的調整方式。

將自訂 HSB 值指派給 [UI \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md) 和 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)時，建議將這些值設為夠高的對比，以確保可讀性。 具體而言，文字色彩應該比功能區 UI 的最亮陰影更深色。 在必要時，架構會自動調整 UI \_ PKEY \_ GlobalTextColor HSB 值，以提供與任何衍生自 UI PKEY GlobalBackgroundColor 之背景陰影或漸層的足夠對比 \_ \_ 。

> [!Note]  
> 在 Windows 7 中，ui [ \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md)可以獨立于[ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)之外進行設定。

 

下列範例示範如何為 [ui \_ PKEY \_ GlobalTextColor](windowsribbon-reference-properties-uipkey-globaltextcolor.md)、 [ui \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md)和 [ui \_ PKEY \_ GlobalHighlightColor](windowsribbon-reference-properties-uipkey-globalhighlightcolor.md) 屬性指定自訂色彩。


```C++
CComPtr<IPropertyStore> spPropertyStore;

// _spFramework is a pointer to the IUIFramework interface that is assigned 
// when the Ribbon is initialized.
if (SUCCEEDED(_spFramework->QueryInterface(&spPropertyStore)))
{
  PROPVARIANT propvarBackground;
  PROPVARIANT propvarHighlight;
  PROPVARIANT propvarText;
 
  // UI_HSBCOLOR is a type defined in UIRibbon.h that is composed of 
  // three component values: hue, saturation and brightness, respectively.
  UI_HSBCOLOR BackgroundColor = UI_HSB(0x14, 0x38, 0x54);
  UI_HSBCOLOR HighlightColor = UI_HSB(0x00, 0x36, 0x87);
  UI_HSBCOLOR TextColor = UI_HSB(0x2B, 0xD6, 0x00);

  InitPropVariantFromUInt32(BackgroundColor, &propvarBackground);
  InitPropVariantFromUInt32(HighlightColor, &propvarHighlight);
  InitPropVariantFromUInt32(TextColor, &propvarText);
 
  spPropertyStore->SetValue(UI_PKEY_GlobalBackgroundColor, propvarBackground);
  spPropertyStore->SetValue(UI_PKEY_GlobalTextColor, propvarText);
 
  spPropertyStore->Commit();
}
```



## <a name="convert-rgb-to-hsb"></a>將 RGB 轉換成 HSB

本節說明將功能區架構 HSB 值（在此範例中為 [UI \_ PKEY \_ GlobalBackgroundColor](windowsribbon-reference-properties-uipkey-globalbackgroundcolor.md) ）動態比對在執行時間的特定 RGB 色彩所需的公式。

索引標籤資料列背景會當做參考點使用，因為它會轉譯為平面色彩介面，相較于功能區背景的亮度漸層。

需要初步轉換才能取得中繼 HSL 值。 這個 HSL 值接著可以轉換成 HSB 值。

> [!Note]  
> 使用大部分的相片編輯軟體，可輕鬆地完成從 RGB 到 HSL 的轉換。

 

從0.0 到 1.0) 範圍中的每個元件轉換 HSL (，到功能區 HSB 設定都是透過下列公式完成：

-   H<sub>background</sub> = Round (255.0 H) 
-   S<sub>背景</sub> = 四捨五入 (255.0 S) 
-   B<sub>背景</sub> = 四捨五入 (257.7 + 149.9 Ln (L) ) if 0.1793 <= L <= 0.9821

## <a name="related-topics"></a>相關主題

<dl> <dt>

[色彩指導方針](https://msdn.microsoft.com/library/aa511283.aspx)
</dt> <dt>

[架構屬性](windowsribbon-reference-properties-framework.md)
</dt> </dl>

 

 





