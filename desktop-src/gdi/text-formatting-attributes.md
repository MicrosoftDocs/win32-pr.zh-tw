---
description: 應用程式可以使用六個函式來設定裝置內容的文字格式屬性： SetBkColor、SetBkMode、SetTextAlign、SetTextCharacterExtra、SetTextColor 和 SetTextJustification。
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Text-Formatting 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e74cb8d30a0eb9b44f05be611da963b413e8798b81da2a334dc083bd3cc1651
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015278"
---
# <a name="text-formatting-attributes"></a>Text-Formatting 屬性

應用程式可以使用六個函式來設定裝置內容的文字格式屬性： [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)、 [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)、 [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)、 [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)、 [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)和 [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)。 這些函式會影響文字對齊、intercharacter 間距、文字對齊方式，以及文字和背景色彩。 此外，還有其他六個函式可用來取出任何裝置內容的目前文字格式屬性： [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)、 [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)、 [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)、 [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)、 [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)和 [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)。

## <a name="text-alignment"></a>文字對齊

應用程式可以使用 [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) 函式來指定系統在呼叫其中一個繪圖函式時，如何將字元放在文字字串中。 您可以使用此函式來定位標題、頁碼、標注等等。 系統會在圍繞字串的虛數矩形上對齊參考點，並以目前的游標位置或將某個點當作引數傳遞至其中一個文字繪圖函式的點，來放置文字字串。 [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign)函數可讓應用程式指定此參考點的位置。 以下是可能的參考點位置清單。



| Location         | 描述                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| 靠左/靠下      | 參考點位於矩形的左下角。                                               |
| 左/基底行   | 參考點位於字元儲存格基底線和矩形左邊緣的交集處。  |
| 左/上         | 參考點位於矩形的左上角。                                                 |
| 中間/底部    | 參考點位於矩形底部的中央。                                            |
| 中心/基底線 | 參考點位於字元儲存格基底線和矩形中央的交集處。     |
| 置中/靠上       | 參考點位於矩形頂端的中央。                                               |
| 右/下     | 參考點位於矩形的右下角。                                              |
| 右/基底線  | 參考點位於字元儲存格基底線和矩形右邊緣的交集處。 |
| 靠右/靠上        | 參考點位於矩形的右上角。                                                |



 

下圖顯示藉由呼叫 [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) 函數繪製的文字字串。 在繪製文字之前，會呼叫 [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) 函式，將參考點重新放置在九個可能位置的每一個位置。

![顯示相同文字九次的圖，每個可能的參考點位置各一個](images/csftx-04.png)

裝置內容的預設文字對齊方式是圍繞文字之虛數矩形的左上角。 應用程式可以藉由呼叫 [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) 函式，來取得任何裝置內容的目前文字對齊設定。

## <a name="intercharacter-spacing"></a>Intercharacter 間距

應用程式可以使用 [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) 函式來改變指定裝置內容中所有文字輸出作業的 intercharacter 間距。 下圖顯示透過呼叫 [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) 函式繪製兩次的文字字串。 第二次繪製文字之前，會呼叫 [**SetTextCharacterExtra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) 函數來遞增 intercharacter 間距。

![圖例 shoing 相同的文字兩次：先具有一般 intercharacter 間距，然後以較寬的間距表示](images/csftx-06.png)

任何裝置內容的預設 intercharacter 間距值為零。 應用程式可以藉由呼叫 [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) 函式，來取得裝置內容的目前 intercharacter 間距值。

## <a name="text-justification"></a>文字對齊方式

應用程式可以使用 [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) 和 [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) 函式來調整一行文字。 文字對齊是在任何桌上型電腦和大部分文書處理應用程式中常見的操作。 [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a)函數會計算文字字串的寬度和高度。 計算寬度之後，應用程式可以呼叫 [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) 函式，以在文字行中的每個單字之間分佈額外的間距。 下圖顯示一段文字列印兩次：在第一個段落中，未對齊文字;在第二個段落中，藉由呼叫 **GetTextExtentPoint32** 和 **SetTextJustification** 函式來對齊文字。

![圖例顯示只靠左對齊的段落，然後靠左和靠右對齊相同段落](images/csftx-05.png)

## <a name="text-and-background-color"></a>文字和背景色彩

應用程式可以使用 [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) 函式來設定在其視窗的工作區中繪製的文字色彩，以及彩色印表機上繪製的文字色彩。 應用程式可以使用 [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) 函式來設定出現在每個字元後面的色彩，並使用 [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) 函式來指定系統應該如何將選取的背景色彩與影片顯示器上目前的色彩或色彩混合。

顯示裝置內容的預設文字色彩為黑色;預設的背景色彩為白色;而且預設的背景模式是不透明的。 應用程式可以藉由呼叫 [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) 函式，來取得裝置內容的目前文字色彩。 應用程式可以藉由呼叫 [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) 函式和目前的背景模式來取得裝置內容目前的背景色彩，方法是呼叫 [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) 函數。

 

 
