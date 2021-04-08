---
title: IAgentBalloon
description: IAgentBalloon
ms.assetid: 94a48cd9-bea5-4993-8991-50c6c86a646b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b811956e368abbaf2d2782c68017084f5e17a09f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681925"
---
# <a name="iagentballoon"></a>IAgentBalloon

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

**IAgentBalloon** 定義了一個介面，可讓應用程式查詢 Microsoft Agent 文字提示的屬性。 這些函數也可從 [**IAgentBalloonEx**](https://www.bing.com/search?q=**IAgentBalloonEx**)取得。

字元的文字氣球的初始預設值是在 Microsoft Agent 字元編輯器中設定，但是在應用程式執行之後，使用者可能會覆寫 [ [**Enabled**](enabled-property.md) ] 和 [ [Font](fontname-property.md) ] 屬性。 如果使用者變更氣球的屬性，變更就會影響所有的字元。 [**IAgentBalloon**](/windows/desktop/lwef/iagentballoon)物件的屬性也適用于透過 [[**思考**](think-method.md)] 方法的文字輸出。

**依照 Vtable 順序的方法**



| IAgentBalloon 方法                                       | Description                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [GetEnabled](iagentballoon--getenabled.md)                 | 傳回是否啟用文字提示。                                          |
| [GetNumLines](iagentballoon--getnumlines.md)               | 傳回文字氣球中顯示的行數。                            |
| [GetNumCharsPerLine](iagentballoon--getnumcharsperline.md) | 傳回文字球中顯示的每一行字元平均字元數。      |
| [GetFontName](iagentballoon--getfontname.md)               | 傳回文字氣球中所顯示字型的名稱。                           |
| [GetFontSize](iagentballoon--getfontsize.md)               | 傳回文字氣球中所顯示字型的大小。                           |
| [GetFontBold](iagentballoon--getfontbold.md)               | 傳回文字批註框中顯示的字型是否為粗體。                       |
| [GetFontItalic](iagentballoon--getfontitalic.md)           | 傳回文字批註框中顯示的字型是否為斜體。                     |
| [GetFontStrikethru](iagentballoon--getfontstrikethru.md)   | 傳回文字氣球中顯示的字型是否顯示為刪除線。 |
| [GetFontUnderline](iagentballoon--getfontunderline.md)     | 傳回文字氣球中顯示的字型是否加上底線。                 |
| [GetForeColor](iagentballoon--getforecolor.md)             | 傳回文字氣球中所顯示的前景色彩。                           |
| [GetBackColor](iagentballoon--getbackcolor.md)             | 傳回文字氣球中所顯示的背景色彩。                           |
| [GetBorderColor](iagentballoon--getbordercolor.md)         | 傳回文字氣球中顯示的框線色彩。                               |
| [SetVisible](iagentballoon--setvisible.md)                 | 將文字批註設定為可見。                                                  |
| [GetVisible](iagentballoon--getvisible.md)                 | 傳回文字氣球的可見度設定。                                  |
| [SetFontName](iagentballoon--setfontname.md)               | 設定文字氣球中使用的字型。                                               |
| [SetFontSize](iagentballoon--setfontsize.md)               | 設定文字氣球中使用的字型大小。                                          |
| [SetFontCharSet](iagentballoon--setfontcharset.md)         | 設定字組氣球中使用的字元集。                                      |
| [GetFontCharSet](iagentballoon--getfontcharset.md)         | 傳回字組氣球中使用的字元集。                                   |



 

 

 