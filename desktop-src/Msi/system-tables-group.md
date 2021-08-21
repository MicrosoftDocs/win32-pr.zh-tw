---
description: 系統資料表群組的資料表會追蹤安裝資料庫的資料表和資料行。
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: 系統資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c05bfd06bcff049d2aea847a2bb8d0c4c3fc3d1443a615f75912ac7d4f86d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623917"
---
# <a name="system-tables-group"></a>系統資料表群組

系統資料表群組的資料表會追蹤安裝資料庫的資料表和資料行。

-   [ \_ 資料表資料表](-tables-table.md)會追蹤資料庫中的所有資料表。 這包括您可能已為自己的自訂動作建立的資料表。 查詢此資料表，以找出資料表是否存在。
-   [ \_ Columns 資料表](-columns-table.md)會追蹤安裝資料庫中的資料行。 此資料表目前未追蹤暫存資料行。 查詢此資料表，以找出指定的資料行是否存在。
-   [ \_ 資料流程資料表](-streams-table.md)會列出內嵌的 OLE 資料流程。
-   [ [ \_ 儲存體] 資料表](-storages-table.md)會列出內嵌的 OLE 資料儲存體。
-   [ \_ 驗證資料表](-validation-table.md)。 \_驗證資料表會追蹤資料庫中每個資料行的類型和允許的範圍。 在 \_ 資料庫驗證過程中，會使用驗證資料表來確保所有資料行都已納入考慮，而且具有正確的值。 此資料表並未隨附于安裝程式資料庫。

 

 



