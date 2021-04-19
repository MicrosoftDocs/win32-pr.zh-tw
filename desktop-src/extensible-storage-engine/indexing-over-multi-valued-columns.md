---
description: 深入瞭解：編制多值資料行的索引
title: 編制多值資料行的索引
TOCTitle: Indexing over Multi-Valued Columns
ms:assetid: 90e31df2-2f5b-47a8-84c1-ece6bcc40858
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269341(v=EXCHG.10)
ms:contentKeyID: 32765630
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: aea24e8423b704b7e0345898bcb6ae4b6d7c057b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974545"
---
# <a name="indexing-over-multi-valued-columns"></a>編制多值資料行的索引


_**適用于：** Windows |Windows Server_

## <a name="indexing-over-multi-valued-columns"></a>編制多值資料行的索引

多值資料行的索引只會對索引中的第一個多重值資料行執行。 第一個多重值資料行會展開，以便將資料行中的每個值編制索引。 所有其他多重值資料行只會在資料行中的第一個值進行索引。 例如，索引是在資料行 A 和資料行 B 上定義，而這兩個數據行都是多重值。 在給定的記錄中，資料行 A 的值為紅色、藍色，而資料行 B 的值為1、2和3。 產生的索引會提供紅色-1 和藍1的專案。 第二個數據行 B 的值則不會展開。 請注意，即使每個標記的資料行都可能是多重值的標記資料行（透過 JET_bitColumnMultiValued 明確標示為多重值），還是會以這種方式展開。 此外，因為主要索引項目包含記錄，所以不允許在多重值資料行上具有主要索引，因為這樣會導致索引中的多個位置在記錄中必須存在。 如需詳細資訊，請參閱 [標記的、固定和變數資料行](./tagged-fixed-and-variable-columns.md) 主題。

從 Windows Vista 開始，使用者可以選擇在使用 [JetCreateIndex](./jetcreateindex-function.md) 或 [JetCreateIndex2](./jetcreateindex2-function.md) 建立索引時，使用 [JET_INDEXCREATE](./jet-indexcreate-structure.md) 結構來設定 JET_bitIndexCrossProduct 選項。 在索引上設定此選項時，會展開索引中的所有多重值索引鍵資料行，並針對這些資料行中的每個值，在索引中建立交叉乘積。 上述範例現在會產生紅-1、red-2、red-3、blue-1、藍2、藍3的專案。 同樣地，每個索引鍵資料行都必須明確宣告為多重值，才能透過 JET_bitColumnMultiValued 在索引中展開。
