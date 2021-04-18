---
description: 動態圖表建立
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: 動態圖表建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971287"
---
# <a name="dynamic-graph-building"></a>動態圖表建立

如果您需要修改現有的篩選圖形，您可以停止圖形、進行變更，然後重新開機圖形。 這通常是最好的方法。 不過，在某些情況下，您可能會想要在圖形仍在執行時加以變更。 例如：

-   應用程式會在播放期間插入影片效果篩選。
-   來源篩選器會切換媒體類型中途，可能需要新的解壓縮篩選器。
-   應用程式會將新的影片串流新增至圖形。

這些都是 *動態圖形建築物* 的範例，這是在圖形繼續執行時涵蓋對篩選圖形任何變更類型的詞彙。 動態圖形建築物可以由應用程式或圖形中的篩選器起始。 可能有三種不同的案例：

-   [動態格式變更](dynamic-format-changes.md)：篩選準則可以變更中途格式，而不需要移除或取代任何篩選準則。
-   [動態重新連接](dynamic-reconnection.md)：藉由加入或移除篩選來變更圖形。
-   [篩選鏈](filter-chains.md)：新增、移除及控制篩選的鏈。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 DirectShow](about-directshow.md)
</dt> </dl>

 

 



