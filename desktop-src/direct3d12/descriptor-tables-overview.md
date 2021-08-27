---
title: 描述項資料表總覽
description: 每個描述中繼資料表都會儲存一或多個類型的描述元-SRVs、UAVe、CBVs 和取樣器。 描述項資料表不是記憶體的配置;它只是描述項堆積中的位移和長度。
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3edae00c37a451aa0fb71355a1dea5860de4398f
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813121"
---
# <a name="descriptor-tables-overview"></a>描述項資料表總覽

每個描述中繼資料表都會儲存一個或多個類型的描述元 &mdash; SRVs、UAVe、CBVs 和取樣器。 描述項資料表不是記憶體的配置;它只是描述項堆積中的位移和長度。

## <a name="referencing-descriptor-tables"></a>參考描述中繼資料表

圖形管線（透過根簽章）藉由依索引參考描述中繼資料表來取得資源的存取權。

描述項資料表實際上只是描述項堆積的子範圍。 描述元堆積代表描述項集合的基礎記憶體配置。 由於記憶體配置是建立描述項堆積的屬性，因此定義一個描述中繼資料表時，一定會比識別堆積中的區域到硬體一樣便宜。 描述中繼資料表不需要在 API 層級建立或終結，它們只會在每次參考時，將它們識別為與堆積的位移和大小。

當應用程式的著色器想要從大量可用的描述項中自由選取時，您當然可以定義非常大的描述中繼資料表， (通常會即時參考紋理)  (可能是以材質資料) 所驅動。

根簽章參考具有堆積參考的描述項資料表專案、資料表的開始位置 (從堆積) 開始的位移，以及資料表) 專案中 (的長度。 下圖顯示下列概念：描述中繼資料表指標的根簽章，以及描述元中的完整紋理或緩衝區資料的描述元中的描述元， (在材質的情況下，預設堆積) 。

![描述中繼資料表](images/descriptor-table.png)

## <a name="related-topics"></a>相關主題

* [描述中繼資料表](descriptor-tables.md)
