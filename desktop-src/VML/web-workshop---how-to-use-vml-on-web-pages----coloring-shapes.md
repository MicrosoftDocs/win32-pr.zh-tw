---
title: 著色圖形
description: 本文描述如何在 VML 中著色圖形，這是 Windows Internet Explorer 9 的已淘汰功能。
ms.assetid: f528f0c7-1351-4bca-b309-67511431b711
keywords:
- 網路研討會，著色圖形
- 設計網頁、著色圖形
- Vector Markup Language (VML) 、著色圖形
- VML (Vector Markup Language) 、著色圖形
- 向量圖形，著色圖形
- VML 圖形，著色
- 著色圖形
- Vector Markup Language (VML) 、關鍵字色彩名稱
- VML (Vector Markup Language) ，關鍵字色彩名稱
- 向量圖形，關鍵字色彩名稱
- 關鍵字色彩名稱
- Vector Markup Language (VML) 、RGB triplet
- VML (Vector Markup Language) ，RGB triplet
- 向量圖形、RGB triplet
- RGB triplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8edd8b067f1e3648d2b69f473c02c59392a10b5716afea74b8f7b0c9d093989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057040"
---
# <a name="coloring-shapes"></a>著色圖形

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需有關 Windows Internet Explorer 目前版本的資訊、建議和指引，請參閱[Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

如先前幾節中所述，您可以使用 "red" 來代表紅色的色彩 "blue" 代表藍色的色彩，依此類推。 在本主題中，我們將說明如何以任何您想要的色彩繪製圖形。

VML 延伸 HTML 和 CSS 色彩語法。 當 VML 專案的屬性型別為 color 時（例如 **fillcolor** 和 **strokecolor** ），您可以使用 [關鍵字色彩名稱](#keyword-color-name) 或 [RGB 三](#rgb-triplet)型來表示色彩。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="keyword-color-name"></a>關鍵字色彩名稱

HTML 4.0 定義關鍵字色彩名稱的清單。 它們是淺綠色、黑色、藍色、fuchsia、灰色、綠色、橙色、暗灰色、navy、橄欖色、紫色、紅色、銀級、青色、白色和黃色。 這16種色彩的 RGB 值會以 [HTML 4.0 規格](https://www.w3.org/TR/REC-html40/types.mdl#h-6-5) 來定義。

例如，您可以藉由指定來繪製填滿黃色的矩形 `fillcolor="yellow"` ，並藉由指定來提供藍色外框 `strokecolor="blue"` ，如下列 VML 標記法所示：

![color1.gif (305 個位元組) ](images/color1.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="yellow" strokecolor="blue"/>
```





[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="rgb-triplet"></a>RGB 三

如果色彩不是 [關鍵字色彩名稱](#keyword-color-name)，您可以將色彩表示為 rgb 十進位數或 rgb 十六進位三個十六進位。 使用 RGB triplet，您可以指定色彩的紅色、綠色和藍色元件的值，將每個元件設定為值範圍從0到255（十進位）或00到 FF （十六進位）。

例如，您可以在指定或的情況下，使用十進位值253、249、186的自訂色彩來建立填滿矩形的矩形 `fillcolor="rgb(253,249, 186)"` ， `fillcolor="#FDF9BA"` 如下列 VML 標記法所示。 在十六進位中，值253會變成 FD、249變成 F9，而186會變成 BA。

![color2.gif (305 個位元組) ](images/color2.gif)


```HTML
<v:rect style='width:120pt;height:80pt;'
fillcolor="#FDF9BA" strokecolor="blue"/>
```





如果 RGB 在十六進位中有像是 XXYYZZ 的模式，您可以將它縮寫為 XYZ。 例如，" \# 66FF99" 可以寫出為 " \# 6F9"。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="summary"></a>總結

在 VML 中，您可以使用下列其中一種格式來表示色彩：

1.  fillcolor = "blue"
2.  fillcolor = "rgb (0，0255) "
3.  fillcolor = " \# 0000ff"

 

 