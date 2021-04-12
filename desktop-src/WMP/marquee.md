---
title: Marquee
description: Marquee
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Windows Media Player 行動外觀、字幕
- 外觀、字幕
- 外觀、字幕的參考
- 外觀中的字幕，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372422"
---
# <a name="marquee"></a>Marquee

[字幕] 是一個滾動文字顯示方塊，可顯示一或多個文字顯示方塊的資訊。 您不需要加入字幕，但是當您有想要在有限空間中顯示給使用者的詳細資訊時，這可能非常有用。

只有在符合下列兩個條件時，才會滾動字幕中的文字：

-   您有比 [字幕] 顯示方塊寬度還多的文字，可顯示在捲動方塊中。
-   媒體專案可能已停止或暫停。

面板定義檔的 [字幕] 區段必須以以下這一行開頭：


```C++
[ Marquee ]

```



> [!Note]  
> 若要維持與 Windows Media Player 10 行動裝置版 Windows Media Player Mobile 的相容性，在面板定義檔中使用 "Marquis" 仍會被視為有效。

 

然後，您必須新增一或多行，其中包含面板中每個字幕顯示方塊的相關資訊。


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



您可以使用下列範本作為面板定義檔的 [字幕] 區段：


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



您必須使用下列順序來取得 [字幕] 區段中每一行的資訊， (行的每個部分都必須) ：

1.  [天棚位置](marquee-location.md)
2.  [天棚字型](marquee-font.md)
3.  [天棚色彩](marquee-color.md)
4.  [文字組合](text-combinations.md)

如需字幕程式碼的範例，請參閱 [範例天棚一節](sample-marquee-section.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**外觀參考**](skin-reference.md)
</dt> </dl>

 

 




