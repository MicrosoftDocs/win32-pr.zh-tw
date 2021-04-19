---
description: 深入瞭解：版本、自動遞增和託管資料行
title: 版本、自動遞增和託管資料行
TOCTitle: Version, Auto-Increment and Escrow Columns
ms:assetid: b12724a4-6846-49a7-9223-43895f91427e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294059(v=EXCHG.10)
ms:contentKeyID: 32765674
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e5966990a51e87b90946416161e20d677116f8c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974121"
---
# <a name="version-auto-increment-and-escrow-columns"></a>版本、自動遞增和託管資料行


_**適用于：** Windows |Windows Server_

## <a name="version-auto-increment-and-escrow-columns"></a>版本、自動遞增和託管資料行

ESE 提供具有特殊功能的版本、自動遞增及擁有的更新資料行類型。 在 [JetAddColumn](./jetaddcolumn-function.md)呼叫中所使用 [JET_COLUMNDEF](./jet-columndef-structure.md)結構的 **grbit** 成員中設定的資料行選項，指出資料行是否為此處所述的其中一種特殊類型。

### <a name="version-jet_bitcolumnversion"></a>版本 (JET_bitColumnVersion) 

[版本資料行] 選項（僅適用于 JET_coltypLong 資料行）表示資料行包含記錄的版本資訊，可用來判斷是否需要重新整理指定記錄的記憶體中複本。 當應用程式透過 [JetUpdate](./jetupdate-function.md)修改資料行時，ESE 會自動遞增版本資料行。

### <a name="auto-increment-jet_bitcolumnautoincrement"></a>自動遞增 (JET_bitColumnAutoincrement) 

當新的記錄插入資料表時，自動遞增資料行會自動由 ESE 遞增。 自動遞增資料行中包含的值對資料表中的每一筆記錄而言是唯一的，而且不保證是連續的。 這些值不會回收，但在某些情況下可以重複使用。 只有 JET_coltypLong 和 JET_coltypLongLong 類型的資料行可以是自動遞增資料行。

### <a name="escrow-jet_bitcolumnescrowupdate"></a>JET_bitColumnEscrowUpdate) 的 (

您可以在 [JetEscrowUpdate](./jetescrowupdate-function.md)的呼叫中修改可修改的「託管」資料行。 進行中的更新是不會受到寫入衝突影響的數值差異作業。 這表示，任何數目的會話都可以透過 [JetEscrowUpdate](./jetescrowupdate-function.md) 並行更新記錄中的已系建資料行，而不會發生衝突。 請注意，任何其他更新作業可能仍會導致與進行中的更新作業發生寫入衝突。 您只能對具有預設值 JET_coltypLong 類型的資料行進行保管更新。 您也必須先將這些資料行加入至資料表，然後再載入資料列。 最後，包含「已建立」更新資料行的資料列可能會設定為支援「資料列完成」回呼 (JET_bitColumnFinalize) 或在參考計數達到零 (JET_bitColumnDeleteOnZero) 時自動刪除。 如需詳細資訊，請參閱 [JET_COLUMNDEF](./jet-columndef-structure.md) 結構。
