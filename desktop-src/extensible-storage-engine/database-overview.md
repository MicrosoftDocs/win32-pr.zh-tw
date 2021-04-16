---
description: 深入瞭解：資料庫總覽
title: 資料庫總覽
TOCTitle: Database Overview
ms:assetid: 6e4ebfab-8bd2-4fcf-9d91-2148a693596c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269290(v=EXCHG.10)
ms:contentKeyID: 32765582
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 473ffc7f11b3688f0f0904ae15a366ef7d6812d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104553207"
---
# <a name="database-overview"></a>資料庫總覽


_**適用于：** Windows |Windows Server_

## <a name="database-overview"></a>資料庫總覽

ESE 資料庫是索引循序存取方法， (用於儲存和取出資料的 ISAM) 。 ESE 資料庫會儲存在單一檔案中，並且由一或多個使用者定義資料表所組成。 資料是以資料表中的記錄來組織，其中包含一或多個使用者定義的資料行。 所建立的索引會針對整個集合或資料表中的一部分記錄提供不同的組織。 使用 ESE API，應用程式可以建立資料指標，以不同順序在資料庫中流覽記錄。 資料表的元素定義如下：

  - 資料 **行**：資料行是資料表中儲存特定類型資訊的欄位。 您可以根據儲存在資料行中的資料類型，固定或可變長度的資料行。 某些資料行（例如標記的資料行）在 **Null** 或設定為預設值時不會使用空格，而且可以包含多個值。

  - **記錄**：記錄是資料行值的集合，這些值具有主鍵所定義的唯一身分識別。

  - **Index**：索引是索引鍵資料行的集合，可定義資料表中記錄的儲存順序。 叢集或主要索引會定義記錄儲存在資料表中的順序。 您可以定義多個索引，以便在資料表中指定不同的排序來進行記錄。 索引也可以根據簡單的準則來限制可見的記錄集，例如記錄中是否存在特定索引鍵資料行值。

  - **Cursor**：資料指標指出資料表中的目前記錄，並使用目前的索引導覽至資料表中的記錄。 資料指標也包含目前已備妥之更新狀態的資訊。

您可以隨時在資料表中新增或移除資料行和索引。 雖然可以定義多個索引，但資料表中的資料會根據 B + 樹狀結構中的主要索引定義，實際儲存並以邏輯方式進行叢集化。 每個次要索引都會儲存在個別的 B + 樹狀結構中，其中只包含儲存在主表中之實際資料的邏輯指標。 如果未定義任何索引，則資料表中的記錄會以插入的順序儲存在 B + 樹狀結構中，並稱為「連續索引」。

這裡的圖表是一個範例，說明如何根據主要索引，將資料表的資料儲存在 B + 樹狀結構中。 主要索引適用于名稱和識別碼，並為員工的辦公室編號建立次要索引。 次要索引的專案會儲存在個別的 B + 樹狀結構中，其中只包含儲存在主表中的記錄指標。 例如，第二個數據表中的 office 編號12348與主表中的記錄3有關。 記錄3包含 office 12348 中員工的資料行值。 如需詳細資訊，請參閱 [資料表主題中的索引](./indexing-in-the-table.md) 。

![ESE_Documentation_tableandrow2](images/Gg269290.ESE_Documentation_tableandrow2(EXCHG.10).gif "ESE_Documentation_tableandrow2")
