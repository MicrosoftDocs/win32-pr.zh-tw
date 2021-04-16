---
title: 範例天棚區段
description: 範例天棚區段
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player 行動外觀、字幕
- 外觀、字幕
- 外觀、字幕的參考
- 外觀、字幕區段中的字幕
- 外觀定義檔，天棚區段
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462388"
---
# <a name="sample-marquee-section"></a>範例天棚區段

下列各行顯示面板定義檔案的一般字幕區段：


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



這會定義顯示標題和作者的標題和作者（如果兩者都已定義）、只定義標題的標題，或是作者的名稱（如果只定義了作者）。 如果未定義任何專案，則不會顯示任何專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Marquee**](marquee.md)
</dt> </dl>

 

 




