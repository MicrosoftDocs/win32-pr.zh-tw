---
title: 範例點陣圖區段
description: 範例點陣圖區段
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Windows Media Player 行動外觀、點陣圖
- 外觀，點陣圖
- 外觀、點陣圖的參考
- 外觀、點陣圖區段中的點陣圖
- 外觀定義檔，點陣圖區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840452"
---
# <a name="sample-bitmap-section"></a>範例點陣圖區段

下列各行顯示面板定義檔的典型點陣圖區段：


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



這會定義五個位圖，用來建立背景影像、停用和推送按鈕的影像、區域按鈕的區域影像，以及用於 trackbars 的超級影像。

> [!Note]  
> 區域和超級點陣圖在 Windows Media Player 10 行動版或更新版本的面板中會被取代。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**點陣圖**](bitmaps.md)
</dt> </dl>

 

 




