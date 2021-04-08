---
title: 屬性的運作方式
description: 屬性的運作方式
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673908"
---
# <a name="how-properties-work"></a>屬性的運作方式

屬性值會儲存在成員變數中。

屬性可透過方法配對來存取。 其中一個方法會提供執行來指定屬性值;其名稱開頭為 put \_ 。 另一個方法會提供實作為抓取屬性值的實值;其名稱開頭為 get \_ 。 介面定義位於 Echo 中。 屬性方法原型位於 Echo. h 中。 它們會在 Echo 中實作為。

接下來的三個章節將示範如何修改現有的屬性方法，以符合您的需求，以及如何新增其他屬性的方法。

-   [用來儲存屬性的變數](variables-to-store-properties.md)
-   [修改尺規屬性](modifying-the-scale-property.md)
-   [新增濕混合屬性](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Echo 範例屬性**](echo-sample-properties.md)
</dt> </dl>

 

 




