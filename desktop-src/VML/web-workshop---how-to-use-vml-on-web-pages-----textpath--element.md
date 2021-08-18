---
title: 使用 Textpath 元素
description: 使用 Textpath 元素
ms.assetid: 7728cdd6-d291-4ec5-b5e0-4a44a7d72eae
keywords:
- 網路研討會，textpath 元素
- 設計網頁、textpath 元素
- Vector Markup Language (VML) 、textpath 元素
- VML (Vector Markup Language) ，textpath 元素
- 向量圖形，textpath 元素
- textpath 元素
- VML 元素，textpath
- VML 圖形，textpath 元素
- Vector Markup Language (VML) 、繪製文字
- VML (Vector Markup Language) 、繪製文字
- 向量圖形，繪製 VML 文字
- 繪製文字
- VML 圖形，繪製文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5db3b76d0c4ad2e56c59cfcf6dd39a2af51317b63ee190f47d794933282b5a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056970"
---
# <a name="using-the-textpath-element"></a>使用 Textpath 元素

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

在本主題中，我們將說明如何使用專案 `<textpath>` 來繪製具有各種樣式的文字。

您可以將子專案放 `<textpath>` 在內部 `<shape>` 或 `<shapetype>` 繪製文字。 然後，您可以使用子項目的屬性屬性 `<textpath>` 來自訂文字。 您也可以使用 `<formulas>` 子項目來定義文字的大綱。

例如，若要建立下圖中顯示的文字，您可以在下方輸入 VML 標記法。 請注意，我們使用 `<shapetype>` 元素來定義文字外框的原型。 然後，從相同的 shapetype 具現化兩個圖形。 您可以直接變更 **字串** 屬性屬性，以顯示不同的文字。

![shape1 \-1.gif (4898 個位元組) ](images/shape1-1t.gif)

![shape1 \-2.gif (2789 個位元組) ](images/shape1-2t.gif)


```HTML
<v:shapetype id="MyShape"
coordsize="21600,21600" adj="9931"
path="m0@0c7200@2,14400@1,21600,0m0@5c7200@6,14400@6,21600@5e">
<v:formulas>
<v:f eqn="val #0"/>
<v:f eqn="prod #0 3 4"/>
<v:f eqn="prod #0 5 4"/>
<v:f eqn="prod #0 3 8"/>
<v:f eqn="prod #0 1 8"/>
<v:f eqn="sum 21600 0 @3"/>
<v:f eqn="sum @4 21600 0"/>
<v:f eqn="prod #0 1 2"/>
<v:f eqn="prod @5 1 2"/>
<v:f eqn="sum @7 @8 0"/>
<v:f eqn="prod #0 7 8"/>
<v:f eqn="prod @5 1 3"/>
<v:f eqn="sum @1 @2 0"/>
<v:f eqn="sum @12 @0 0"/>
<v:f eqn="prod @13 1 4"/>
<v:f eqn="sum @11 14400 @14"/>
</v:formulas>
<v:path textpathok="t" />
<v:textpath on="t" fitshape="t" xscale="t"/>
</v:shapetype>

<v:shape type="#MyShape" style='position:relative; top:5; left:5;
width:261.6pt;height:71.45pt;' adj="8717" fillcolor="red" strokeweight="1pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/> <v:textpath
style='font-family:"Arial Black";v-text-kern:t' trim="t"
fitpath="t" xscale="f" string="Hello World !"/>
</v:shape>

<v:shape type="#MyShape" style='position:relative; top:120; left:5; width:207pt;
height:63pt;' adj="8717" fillcolor="blue" strokeweight="2pt">
<v:fill method="linear sigma" focus="100%" type="gradient"/>
<v:shadow on="t" offset="3pt"/>
<v:textpath style='font-family:"Times New Roman";v-text-kern:t'
trim="t" fitpath="t" xscale="f" string="VML"/>
</v:shape>
```





如需此元素的詳細資訊，請參閱 [VML 規格](https://www.w3.org/TR/NOTE-VML#-toc416858398) 。

 

 