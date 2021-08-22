---
title: 外觀定義檔
description: 外觀定義檔
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- 面板定義檔 Windows Media Player 的外觀
- 外觀、面板定義檔
- 面板的檔案、外觀定義
- 外觀定義檔，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf162870596968872c4f146772c9e62277f5b2ccb660270794248786a71355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995238"
---
# <a name="skin-definition-file"></a>外觀定義檔

面板定義檔包含外觀的基本指示，以及可以找到面板所使用之其他檔案的位置。 面板只能有一個面板定義檔案，且其副檔名為 wms。

面板定義檔中的指示是以可延伸標記語言 (XML)  (XML) 來撰寫，類似于 HTML。 如果您已經使用 HTML 來建立網頁，您會發現 XML 看起來很熟悉。

面板定義檔中的 XML 會使用一組特殊元素標記，來定義面板使用者介面的元件。 例如， [button](button-element.md) 元素會定義按鈕的行為方式、其所在位置，以及它的外觀。

每個元素標記都有特定屬性。 例如， [button](button-element.md) 元素具有 **影像** 屬性，可定義可在何處找到按鈕的圖片。 這類似于 HTML，其中 BODY 元素會 **有一個 background** 屬性，可定義 html 網頁的背景色彩。 所有面板元素及其屬性的詳細資訊都包含在 [面板程式 [設計參考](skin-programming-reference.md) ] 區段中。

XML 有幾個簡單的規則，您必須知道這些規則才能建立外觀。 與 HTML 不同的是，XML 需要您完全遵循規則。

## <a name="enclose-elements-with-angle-brackets"></a>以角括弧括住元素

所有元素都以角括弧括住;例如， **BUTTON** 元素的類型如下：


```C++
<BUTTON>

```



您不需要在所有大寫字母中輸入 "BUTTON" 一字，但在此 SDK 的範例程式碼中，會使用以全部大寫輸入元素名稱的慣例。

## <a name="put-attributes-before-the-closing-bracket"></a>將屬性放在右括弧之前

特定元素的所有屬性都必須包含在右角括弧前面。 屬性是由屬性名稱後面接著等號 (=) 和屬性的值以引號括住。


```C++
<BUTTON image="mypic.jpg">

```



您不需要在小寫中輸入 "image" 這個字，但在此 SDK 的範例程式碼中，會使用以小寫輸入屬性名稱的慣例。 另請注意，屬性的值會以引號括住。

## <a name="opening-and-closing-elements"></a>開啟和關閉元素

某些專案會在另一個元素內群組在一起。 例如，除非您將一或多個 **BUTTONELEMENT** 元素與它搭配使用，否則 **BUTTONGROUP** 元素不會有很大的意義。 若要讓群組清楚，您需要為每個專案都有開頭和結束記號。 開頭的標記只是元素名稱和任何相關的屬性（以角括弧括住）。 結束記號是元素名稱，前面加上正斜線 (/) ，然後以角括弧括住。 例如， **BUTTONGROUP** 元素開啟標記如下所示：


```C++
<BUTTONGROUP>

```



結尾 **BUTTONGROUP** 標記如下所示：


```C++
</BUTTONGROUP>

```



您會將 **BUTTONELEMENT** 標記放在開頭和結尾的 **BUTTONGROUP** 元素標記之間。 例如：


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a>關閉元素

如果專案內沒有其他專案，則您必須在專案名稱的結尾加上正斜線（緊接在右角括弧前面）。 例如，在上述程式碼中，每個 **BUTTONELEMENT** 專案都有一個正斜線，表示其中沒有任何其他專案嵌套在其中。

換句話說，您必須要有結尾元素標記，或關閉具有正斜線的元素。

這是正確的：


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



不正確：


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



這也不正確：


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



下一節提供有關外觀定義檔案的詳細資訊：

-   [外觀定義檔案結構](skin-definition-file-structure.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**面板檔案**](skin-files.md)
</dt> </dl>

 

 




