---
description: 深入瞭解：多重值的稀疏資料行
title: 多重值的稀疏資料行
TOCTitle: Multi-Valued Sparse Columns
ms:assetid: 36e82a73-aad4-4e0d-a743-a2182c41fe9c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269225(v=EXCHG.10)
ms:contentKeyID: 32765527
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 21dbe18be8be26af9fe32d9b80cbd5744c172793e27701d46438df4d63dcf395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115578"
---
# <a name="multi-valued-sparse-columns"></a>多重值的稀疏資料行


_**適用于：** Windows |Windows伺服器_

## <a name="multi-valued-sparse-columns"></a>多重值的稀疏資料行

稀疏資料行可以是固定或可變的長度，而且是唯一的，因為它們如果是 Null 或保留為預設值，就不會佔用記錄中的空間。 稀疏資料行（也稱為標記資料行）可以在單一記錄中包含一個以上的值。 標記的資料行可以是 [JET_coltyp](./jet-coltyp.md) 常數中所述的任何資料行類型。 當您將資料行加入至資料表時，會在呼叫[JetAddColumn](./jetaddcolumn-function.md)的[JET_COLUMNDEF](./jet-columndef-structure.md)結構中設定 JET_bitColumnTagged 旗標，或在[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)或[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)的呼叫中使用的[JET_COLUMNCREATE](./jet-columncreate-structure.md)結構中設定旗標，來建立資料行。 JET_coltypLongText 和 JET_coltypLongBinary 類型的資料行會自動建立為已標記的資料行。

只有標記的資料行可以在記錄中包含多個值，固定或可變長度的資料行可能不包含多個值。 有兩種類型的多重值資料行：

  - 標記的資料行預設為多重值。 當第二個值加入至資料行時，它會自動變成多重值。

  - 在[JetAddColumn](./jetaddcolumn-function.md)的呼叫中，以[JET_COLUMNDEF](./jet-columndef-structure.md)結構中的 JET_bitColumnMultiValued 選項建立的標記資料行。

JET_bitColumnMultiValued 選項會變更資料行的索引方式。 具有 JET_bitColumnMultiValued 選項的多重值資料行，會比標記的多重值資料行更廣泛地進行索引。 這些資料行會針對多重值資料行中的所有值編制索引，而標記的多重值資料行則只會針對多重值資料行中的第一個值編制索引。 例如，假設有一個多重值資料行，其中 JET_bitColumnMultiValued 選項已設定，而且它是索引中的第一個多重值資料行。 此資料行包含三個值： A、B 和 C。此資料行的索引包含所有三個值的專案： A、B 和 C。如果未設定 JET_bitColumnMultiValued 選項，則這個資料行上的索引只會包含索引中的第一個值（A）。
