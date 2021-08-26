---
title: SVG 支援
description: 從 Windows 10 周年更新開始，Direct2D 支援轉譯包含 svg 圖像大綱的色彩字型，如 OpenType 規格中所述 (參閱「SVG」資料表) 。
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8c5f34531264f95c3617d1324079895b6444cbdbc776d5468fe51fc9890992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917098"
---
# <a name="svg-support"></a>SVG 支援

從 Windows 10 周年更新開始，Direct2D 支援包含 svg 圖像大綱的轉譯[色彩](../directwrite/color-fonts.md)字型（如[OpenType 規格](/typography/opentype/spec/)中所述） (參閱[SVG 表格](/typography/opentype/spec/svg)) 。 從 Windows 10 Creators Update 開始，Direct2D 也支援呈現獨立 SVG 影像。 不過，在 OpenType SVG 字型內不允許某些 SVG 功能，而且 Direct2D 目前不支援某些 SVG 功能。  

本主題指出 Windows 10 周年更新和更新版本中，Direct2D 所支援的[SVG 1.1](https://www.w3.org/TR/SVG11/)功能集。 本檔適用于 OpenType 字型中的 SVG，以及獨立 SVG 影像。

## <a name="supported-svg-elements-and-attributes"></a>支援的 SVG 元素和屬性

Direct2D 支援轉譯下列 SVG 元素，以及每個專案的相關屬性。 系統會忽略其他元素和一般屬性。



| 元素                                                                                  | 支援的一般屬性                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [圈](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | 識別碼、樣式、轉換、cx、cy、r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | 識別碼、樣式、轉換、clipPathUnits                                                      |
| [defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | 識別碼、樣式、轉換                                                                     |
| [desc](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [橢圓](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | 識別碼、樣式、轉換、cx、cy、rx、ry                                                     |
| [G](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | 識別碼、樣式、轉換                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | 識別碼、樣式、轉換、x、y、寬度、高度、preserveAspectRatio、xlink： href               |
| [line](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | id、style、transform、x1、y1、x2、y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | id、style、x1、y1、x2、y2、gradientUnits、gradientTransform、spreadMethod、xlink： href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | 識別碼、樣式、轉換、d                                                                  |
| [多邊形](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | 識別碼、樣式、轉換、點                                                             |
| [折線](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | 識別碼、樣式、轉換、點                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | id、style、cx、cy、r、fx、2006、gradientUnits、gradientTransform、spreadMethod、xlink： href |
| [矩形](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | 識別碼、樣式、轉換、x、y、寬度、高度、rx、ry                                        |
| [停止](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | id、style、offset                                                                        |
| [Svg](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | id、style、x、y、width、height、viewBox、preserveAspectRatio                             |
| [標題](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | 識別碼、樣式、轉換、x、y、寬度、高度、xlink： href                                    |



 

<sup>\*</sup>只有 Windows 10 Creators Update 和更新版本才支援

## <a name="supported-svg-presentation-attributes"></a>支援的 SVG 呈現屬性

Direct2D 也支援下列展示屬性。 您可以在任何 SVG 元素上指定這些專案，但它們只會影響 SVG 規格中所述之特定專案的外觀 (查看 [呈現屬性](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)) 。

-   剪輯路徑
-   剪輯-規則
-   color
-   顯示<sup>\*</sup>
-   fill
-   填滿-不透明度
-   填滿規則
-   不透明度
-   Overflow - 溢位
-   停止色彩
-   停止-不透明度
-   stroke (衝程)
-   筆劃-dasharray
-   筆劃-dashoffset
-   筆劃-linecap
-   筆劃-linejoin
-   筆劃-miterlimit
-   筆劃-不透明度
-   筆劃寬度
-   知名度<sup>\*</sup>

<sup>\*</sup>只有 Windows 10 Creators Update 和更新版本才支援

## <a name="unsupported-svg-features"></a>不支援的 SVG 功能

### <a name="unsupported-elements-and-attributes"></a>不支援的元素和屬性

Direct2D 不會將任何未包含在上述清單中的元素或屬性視為不受支援。 剖析包含不支援之元素或屬性的 SVG 內容時，會忽略不支援的實體。 其餘內容會盡可能地轉譯。

### <a name="unsupported-length-units"></a>不支援的長度單位

Windows 10 周年更新時，Direct2D 只支援使用者空間長度值和百分比長度值。 不支援具有單位尾碼的長度（例如 "mm" 或 "em"）。

從 Windows 10 Fall Creators Update 開始，Direct2D 也支援絕對單位識別碼： px、pt、pc、cm、mm 和 in。 不支援相對單位識別碼 (em，例如) 。

### <a name="unsupported-image-sources"></a>不支援的影像來源

只有在 xlink： href 屬性設定為 base64 編碼的影像時，才支援 image 元素。 不支援遠端參考。

 

 