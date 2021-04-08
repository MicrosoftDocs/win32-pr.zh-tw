---
title: 點陣圖區段
description: 點陣圖區段
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Windows Media Player 行動外觀、點陣圖
- 外觀，點陣圖
- 建立外觀、點陣圖區段
- 撰寫程式碼的外觀、點陣圖區段
- 外觀、點陣圖區段中的點陣圖
- 外觀定義檔，點陣圖區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4a5e41e8e2b095b199a072e31abde3c1cbaa29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021365"
---
# <a name="bitmaps-section"></a>點陣圖區段

接下來，您必須有定義每個點陣圖檔案的區段。 您將使用的每種點陣圖類型都必須有一個指派的檔案，不過您可以使用相同的點陣圖來擁有多個類型。


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



點陣圖區段的開頭必須是以括弧括住的單字點陣圖，然後是您想要定義的每個點陣圖類型的行。 在此範例中，已定義五種類型的點陣圖。 如需點陣圖區段的詳細資訊，請參閱面板參考中的 [點陣圖](bitmaps.md) 。

> [!Note]  
> 區域和超級點陣圖在 Windows Media Player 10 個行動裝置版或更新版本的外觀中已被取代。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**撰寫程式碼**](writing-the-code.md)
</dt> </dl>

 

 




