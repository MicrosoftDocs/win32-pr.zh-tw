---
title: 描述項資料表總覽
description: 每個描述中繼資料表都會儲存一或多個類型的描述元-SRVs、UAVe、CBVs 和取樣器。 描述項資料表不是記憶體的配置;它只是描述項堆積中的位移和長度。
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104213"
---
# <a name="descriptor-tables-overview"></a>描述項資料表總覽

每個描述中繼資料表都會儲存一或多個類型的描述元-SRVs、UAVe、CBVs 和取樣器。 描述項資料表不是記憶體的配置;它只是描述項堆積中的位移和長度。

-   [參考描述中繼資料表](#referencing-descriptor-tables)
-   [相關主題](#related-topics)

## <a name="referencing-descriptor-tables"></a>參考描述中繼資料表

圖形管線（透過根簽章）藉由依索引參考描述中繼資料表來取得資源的存取權。

描述項資料表實際上只是描述項堆積的子範圍。 描述元堆積代表描述項集合的基礎記憶體配置。 由於記憶體配置是建立描述項堆積的屬性，因此定義一個描述中繼資料表時，一定會比識別堆積中的區域到硬體一樣便宜。 描述中繼資料表不需要在 API 層級建立或終結，它們只會在每次參考時，將它們識別為與堆積的位移和大小。

當應用程式的著色器想要從大量可用的描述項中自由選取時，您當然可以定義非常大的描述中繼資料表， (通常會即時參考紋理)  (可能是以材質資料) 所驅動。

根簽章參考具有堆積參考的描述項資料表專案、資料表的開始位置 (從堆積) 開始的位移，以及資料表) 專案中 (的長度。 下圖顯示這些概念：描述中繼資料表指標來自根簽章，以及描述項堆積內的描述元，參考上傳堆積中的完整紋理或緩衝區資料。

![描述中繼資料表](images/descriptor-table.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[描述中繼資料表](descriptor-tables.md)
</dt> </dl>

 

 




