---
title: VML TextPath 元素
description: VML TextPath 元素
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08707ae79bf297e6094228b26ae118c57a03c736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968905"
---
# <a name="vml-textpath-element"></a>VML TextPath 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

定義圖形的文字路徑。

下列屬性會修改文字路徑。



| 屬性                                                                    | 描述                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [FitPath](msdn-online-vml-fitpath-attribute.md)                             | 定義文字是否符合圖形的路徑。                             |
| [FitShape](msdn-online-vml-fitshape-attribute.md)                           | 定義文字是否符合圖形界限。                            |
| [Font-family](msdn-online-vml-font-family-attribute.md)                     | 指定文字的字型系列。                                             |
| [字型大小](msdn-online-vml-font-size-attribute.md)                         | 指定文字的字型大小。                                               |
| [字型樣式](msdn-online-vml-font-style-attribute.md)                       | 指定文字的字型樣式。                                              |
| [字型-Variant](msdn-online-vml-font-variant-attribute.md)                   | 指定文字的字型變化。                                            |
| [字型粗細](msdn-online-vml-font-weight-attribute.md)                     | 指定文字的字型粗細。                                             |
| [字型](msdn-online-vml-font-attribute.md)                                   | 指定文字的複合字型大小值。                                     |
| [MSO-文字陰影](msdn-online-vml-mso-text-shadow-attribute.md)             | 定義是否要將陰影套用至文字。                               |
| [開啟](on-attribute--textpath--vml.md)                                        | 定義是否顯示文字。                                         |
| [String](msdn-online-vml-string-attribute.md)                               | 定義文字字串。                                                       |
| [文字裝飾](msdn-online-vml-text-decoration-attribute.md)             | 定義文字的文字裝飾。                                       |
| [修剪](msdn-online-vml-trim-attribute.md)                                   | 定義是否要在文字的上方和下方移除額外的空間。               |
| [V-旋轉-字母](msdn-online-vml-v-rotate-letters-attribute.md)           | 決定是否旋轉文字的字母。                        |
| [V 相同的字母高度](msdn-online-vml-v-same-letter-heights-attribute.md) | 判斷所有字母的高度是否都相同。                      |
| [V-文字對齊](msdn-online-vml-v-text-align-attribute.md)                   | 定義文字的對齊方式。                                             |
| [V 文字間距](msdn-online-vml-v-text-kern-attribute.md)                     | 決定是否開啟字偶間距調整。                                       |
| [V-文字-反轉](msdn-online-vml-v-text-reverse-attribute.md)               | 決定是否反轉資料列的版面配置順序。                       |
| [V-文字-間距-模式](msdn-online-vml-v-text-spacing-mode-attribute.md)     | 定義字母間距的模式。                                            |
| [V-文字間距](msdn-online-vml-v-text-spacing-attribute.md)               | 定義文字的間距量。                                        |
| [XScale](msdn-online-vml-xscale-attribute.md)                               | 決定是否要使用直接 textpath，而不是圖形路徑。 |



 

**備註**

這個元素必須定義在 [Shape](shape-element--vml.md) 元素內。

除了一般填滿、字串和樣式屬性之外， [Path](msdn-online-vml-path-element.md)的 [TextPathOK](msdn-online-vml-textpathok-attribute.md)屬性必須設定為 **True** ，而 TextPath 的 [On](on-attribute--textpath--vml.md)屬性必須設定為 **true** ，才能在文字路徑上顯示文字。

以下是在路徑上顯示文字所需的最少程式碼。


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**範例**

-   [簡單 TextPath 範例](/previous-versions/bb264038(v=vs.85))
-   [Dynamic TextPath 字樣範例](/previous-versions/bb264042(v=vs.85))
-   [動態 TextPath 曲線範例](/previous-versions/bb264041(v=vs.85))

 

 