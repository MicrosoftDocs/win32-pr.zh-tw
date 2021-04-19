---
description: 從查詢傳回結果之後，您可以存取資料列集的數個屬性。
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: 資料列集屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997078"
---
# <a name="rowset-properties"></a>資料列集屬性

從查詢傳回結果之後，您可以存取資料列集的數個屬性。

除了標準的 OLE DB 資料列集屬性之外，Windows Search SQL 還提供下列四個自訂屬性。 這個屬性集的 GUID 是 {AA6EE6B0E828-11D0-B23E-00AA0047FC01}。

Windows Search 支援 DBPROPSET 資料列集屬性集的標準 OLE DB 屬性 DBPROP \_ COMMANDTIMEOUT。 [ \_ ](/previous-versions//ms691738(v=vs.85))



| 屬性名稱                  | PROPID/類型 | Description                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DONOTCOMPUTEEXPENSIVEPROPS     | 15/VT \_ BOOL | 將此設定為 true，可避免在存取任何資料列集屬性時，計算昂貴的屬性，例如所找到的結果，以及需要評估整個查詢的最大排名。                                                                                                                                                                         |
| 最大排名 (最大 \_ 排名)        | 6/VT \_ I4    | 針對任何結果計算的最高等級。                                                                                                                                                                                                                                                                                                          |
| 找到 (結果的結果 \_)  | 7/VT \_ I4    | 此查詢的唯一專案總數。 針對 SELECT 查詢，這是資料列集中的專案數。 對於查詢的群組，這是唯一分葉專案的數目。 這個屬性不會識別最上層資料列集中的資料列數目 (最上層群組) 的數目。                                                        |
| 其中 ID (WHEREID)              | 8/VT \_ I4    | 用於查詢之限制的識別碼。 如果在執行新查詢時開啟資料列集，新的查詢就可以重複使用較舊查詢中的限制，藉以充分利用已完成的工作。 如需重複使用 WHERE 限制的詳細資訊，請參閱 [ReuseWhere 函數](-search-sql-reusewhere.md)。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 Windows 7 中編制優先順序和資料列集事件的索引](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
