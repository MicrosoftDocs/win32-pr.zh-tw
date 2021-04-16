---
description: 深入瞭解：多重值資料行中的排序
title: 多重值資料行中的排序
TOCTitle: Sequencing in Multi-Valued Columns
ms:assetid: 825a1e51-6b18-4bcf-87f2-4223f302186c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269319(v=EXCHG.10)
ms:contentKeyID: 32765609
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 54f4bd7734cb8c1bf5a87eb444c3205d89f4a6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571534"
---
# <a name="sequencing-in-multi-valued-columns"></a>多重值資料行中的排序


_**適用于：** Windows |Windows Server_

## <a name="sequencing-in-multi-valued-columns"></a>多重值資料行中的排序

多重值資料行中的值是由稱為 *itagSequence* 的索引編號來識別。 此數位是資料行單一值的參考。 當您在資料行中設定、抓取或列舉新值時，會使用這個數位。 *ItagSequence* 適用于各種結構，包括：

  - [JET_RETINFO](./jet-retinfo-structure.md)

  - [JET_SETINFO](./jet-setinfo-structure.md)

  - [JET_SETCOLUMN](./jet-setcolumn-structure.md)

  - [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md)

  - [JET_ENUMCOLUMNVALUE](./jet-enumcolumnvalue-structure.md)

針對多重值資料行中的每個值，此 *itagSequence* 會從1開始。 當新的值加入至資料行時，序號會增加。 在 *itagSequence* 為0的資料行中設定值，表示值會附加至已經在該資料行中的值集合。 使用大於目前為數據行所設定之值數目的 *itagSequence* ，將會有相同的效果。 指定現有值的 *itagSequence* 將會覆寫該值，而不是插入新值。 將現有的值設定為 Null，將會從已在該資料行中的值集合中移除該值。 這會將資料行中的所有後續值向下移動一個位置，讓 *itagSequence* 後續存取這些值的數位小於先前使用的數位。

下圖顯示多重值資料行中的 *itagSequence* 。 名為 ColA 的資料行有三個專案： Val1、Val2 和 Val3，分別 *itagSequence* 為1、2和3。

![ESE_Documentation_TagFixVar](images/Gg269304.ESE_Documentation_TagFixVar(EXCHG.10).gif "ESE_Documentation_TagFixVar")
