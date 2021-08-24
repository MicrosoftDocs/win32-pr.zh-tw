---
description: 深入瞭解：資料表中的索引編制
title: 資料表中的索引編制
TOCTitle: Indexing in the Table
ms:assetid: d86c2c6b-d001-468d-ab74-937911b0036d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294106(v=EXCHG.10)
ms:contentKeyID: 32765721
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 8bfc5054e5fd2b2f13747b0b5729987b9f81d5c21aa2faf38385b11e757f6763
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721448"
---
# <a name="indexing-in-the-table"></a>資料表中的索引編制


_**適用于：** Windows |Windows伺服器_

## <a name="indexing-in-the-table"></a>資料表中的索引編制

索引是一組索引鍵資料行，可定義資料表中記錄的持續順序。 記錄是主要索引中的索引項目。 您可以定義一個主要索引和多個次要索引，以在資料表中建立不同的資料順序。

雖然可以定義多個索引，但記錄實際上是以主要索引所指定的順序儲存在 B + 樹狀結構中。 主要索引一律是叢集索引，而且也必須是唯一的。 主要索引必須在第一個資料表更新之前宣告，以保留索引順序。 當應用程式未定義任何主要索引時，資料會依照記錄新增至資料表的順序儲存。 這個特殊索引稱為「連續索引」。

不同的 B + 樹狀結構是用來根據次要索引來排序記錄。 次要索引中的索引項目會包含根據主要索引所儲存之資料的指標。 主要索引中記錄的索引項目目必須是唯一的，因為次要索引會使用記錄的主鍵指向記錄。 次要索引不一定有唯一性條件約束。 如需詳細資訊，請參閱 [資料庫總覽](./database-overview.md) 主題。
