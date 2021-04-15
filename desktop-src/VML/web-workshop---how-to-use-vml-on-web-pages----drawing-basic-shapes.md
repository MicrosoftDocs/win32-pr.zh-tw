---
title: 繪製基本圖形
description: 本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。
ms.assetid: 05443e1f-c098-441c-a5bc-274cc37ef074
keywords:
- 網路研討會，繪製圖形
- 設計網頁、繪製圖案
- Vector Markup Language (VML) 、繪製圖案
- VML (Vector Markup Language) 、繪製圖案
- 向量圖形，繪製圖形
- 繪製圖案
- VML 圖形，繪圖
- Vector Markup Language (VML) 、XML
- VML (Vector Markup Language) 、XML
- 向量圖形，XML
- Vector Markup Language (VML) 、CSS2
- VML (Vector Markup Language) 、CSS2
- 向量圖形、CSS2
- Vector Markup Language (VML) 、元素
- VML (Vector Markup Language) 、元素
- 向量圖形，元素
- VML 元素，繪製圖形
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ab25fc9310750c9f49c5978a063c76639ec4bd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463592"
---
# <a name="drawing-basic-shapes"></a>繪製基本圖形

本主題說明 VML，這是 Windows Internet Explorer 9 淘汰的功能。 依賴 VML 的網頁和應用程式應該遷移至 SVG 或其他廣泛支援的標準。

> [!Note]  
> 從2011年12月起，本主題已封存。 因此，它不會再主動維護。 如需詳細資訊，請參閱封存的 [內容](/previous-versions/windows/internet-explorer/ie-developer/)。 如需目前 Windows Internet Explorer 版本的相關資訊、建議和指引，請參閱 [Internet Explorer 開發人員中心](https://msdn.microsoft.com/ie/)。

 

在本主題中，我們將說明使用 VML 繪製圖形有多麼容易。

若要在網頁上建立紅色橢圓（如下圖所示），您可以使用圖形編輯工具繪製 oval、將繪圖儲存為點陣圖，然後將點陣圖插入網頁上：

![oval1.gif (627 個位元組) ](images/oval1.gif)

或者，您也可以使用 VML 來繪製圖形。 在上述範例中，您可以在網頁的區域中輸入下列幾行， `<BODY>` 以繪製紅色橢圓形：


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```





`<v:...>` 和 `</v:...>` 是 [XML 語法](#xml-structure)中的開始標記和結束標記。`style='width:100pt; height:75pt'` 提供 [CSS 資訊](#css-information)。 **oval** 和 **fillcolor**= "red" 為 [VML 元素](#vml-elements)。

您只要變更了 VML 中的屬性屬性，就可以改變圖形。 在上述範例中，如果您變更 `fillcolor="red"` 為 `fillcolor="blue"` ，如下列 VML 標記法所示，紅色橢圓將會變更為藍色：


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="blue"> </v:oval>
```





支援 VML 的瀏覽器可以轉譯和顯示 VML 中表示的圖形，而不需要下載個別的影像檔案。 在多個瀏覽器中呈現的大部分圖形都能更快轉譯，而且需要較少的磁碟空間和下載時間。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="xml-structure"></a>XML 結構

根據可延伸標記語言 (XML)  (XML) 的規則來格式化 VML。 任何標準 XML 剖析器都可以剖析 VML，並將產生的資料交給 VML 特定的處理器。 您必須輸入一些資訊，例如 [命名空間](web-workshop---how-to-use-vml-on-web-pages----appendix.md) 和 [內嵌的自訂物件](web-workshop---how-to-use-vml-on-web-pages----appendix.md)，才能讓瀏覽器知道如何將資料交給 VML 特定的處理器。 然後，您可以使用 VML 在區域中輸入圖形， `<BODY>` 就如同您在上述範例中所做的一樣。

`"v:"`每個 XML 標記上的前置詞會將標記識別為 VML。 `"v:"`區域中的前置詞 `<BODY>` 應該與一致 `<html xmlns:v="...">` 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="css-information"></a>CSS 資訊

VML 使用 [階層式樣式表、層級 2 (CSS2) ](https://www.w3.org/TR/PR-CSS2/) 來判斷圖形的大小，以及在網頁上放置圖形。 在上述範例中，我們將 oval 的大小指定為100點 (寬度) 75 點 (高度)  (`style='width:100pt;height:75pt'` ) 。

[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="vml-elements"></a>VML 元素

在上述範例中，我們使用了 VML 預先定義的專案 `<oval>` 來繪製橢圓形。 接著，我們使用專案的 **fillcolor** 屬性屬性 `<oval>` ，以紅色填滿橢圓。

根據[XML 1.0 規格](https://www.w3.org/TR/REC-xml)的[開始標記、結束標記和 Empty-Element 標記](https://www.w3.org/TR/REC-xml#sec-starttags)區段，空的元素標記可用於沒有內容的任何元素。 例如，如下列 VML 標記法所示，元素中沒有任何內容 (子項目) `<oval>` 。  (請注意， **style** 和 **fillcolor** 是元素的屬性， `<oval>` 不是子項目。 ) 


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red"> </v:oval>
```



因此，您可以使用空白元素標記（如下列 VML 標記法所示）來表示與上述程式碼相同的內容。


```HTML
<v:oval style='width:100pt;height:75pt' fillcolor="red" />
```



[![回到 ](images/top.gif) 頂端回到頁首](#top)

## <a name="summary"></a>總結

您可以使用 VML 在網頁上繪製圖形，然後藉由直接變更其屬性屬性來自訂這些圖形。 此外，在多個瀏覽器中呈現的大部分圖形都會以較快的速度轉譯，並縮短下載時間和磁碟空間。

 

 