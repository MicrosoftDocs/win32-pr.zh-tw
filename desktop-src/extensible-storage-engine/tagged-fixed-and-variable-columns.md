---
description: 深入瞭解：標記、固定和變數資料行
title: 標記、固定和變數資料行
TOCTitle: Tagged, Fixed and Variable Columns
ms:assetid: 78a905b8-71a9-4b2e-b9f2-c81bfe3aef8e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269304(v=EXCHG.10)
ms:contentKeyID: 32765595
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: af2ab8ece57342f211b0dd4488b6feb25b191c1977ae39038fb61ea56f20d543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484737"
---
# <a name="tagged-fixed-and-variable-columns"></a>標記、固定和變數資料行


_**適用于：** Windows |Windows伺服器_

## <a name="tagged-fixed-and-variable-columns"></a>標記、固定和變數資料行

標記、固定和可變長度的資料行是 ESE 所支援的主要資料行類型。 標記的資料行不存在於記錄中，除非資料儲存在資料行中，而且可能是固定或可變長度。 標記的資料行也可以在單一記錄中包含一個以上的值。 固定資料行在每個資料列中都採用相同的空間量，且需要1個位來表示 Null 值。 變數長度資料行需要2個位元組來表示大小和 Null 值，而且會佔用每一筆記錄中的可變空間量。 如需已標記和固定資料行的詳細資訊，請參閱 Jet_bitColumnTagged，以及 [JetAddColumn](./jetaddcolumn-function.md)呼叫中所使用 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **grbit** 成員中的 Jet_bitColumnFixed 選項。

可變長度的資料行是由 [JetAddColumn](./jetaddcolumn-function.md)呼叫中的 *coltyp* 參數所設定的資料行類型所決定。 根據是否已設定 Jet_bitColumnFixed 選項，下列資料行類型可以是固定或可變長度：

  - JET_coltypBinary

  - JET_coltypText

  - JET_coltypLongBinary

  - JET_coltypLongText

一般而言，記錄中的資料會先與固定範圍、變數範圍下一，以及最後儲存的標記範圍一起儲存。 下圖顯示如何將記錄儲存在資料表中。 如圖所示，標記的範圍可能包含具有多個值的資料行。

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
