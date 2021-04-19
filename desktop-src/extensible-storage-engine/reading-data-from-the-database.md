---
description: 深入瞭解：從資料庫讀取資料
title: 從資料庫讀取資料
TOCTitle: Reading Data from the Database
ms:assetid: c3c48918-ccd6-4c34-849c-93bd7533ce92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294080(v=EXCHG.10)
ms:contentKeyID: 32765695
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 176cd3189dd1c2701331eff0ef5387827da19b94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971835"
---
# <a name="reading-data-from-the-database"></a><span data-ttu-id="d688a-103">從資料庫讀取資料</span><span class="sxs-lookup"><span data-stu-id="d688a-103">Reading Data from the Database</span></span>


<span data-ttu-id="d688a-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d688a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="reading-data-from-the-database"></a><span data-ttu-id="d688a-105">從資料庫讀取資料</span><span class="sxs-lookup"><span data-stu-id="d688a-105">Reading Data from the Database</span></span>

<span data-ttu-id="d688a-106">從資料庫讀取資料時，應該在交易內執行。</span><span class="sxs-lookup"><span data-stu-id="d688a-106">Reading data from the database should be performed within a transaction.</span></span>

<span data-ttu-id="d688a-107">下列程式說明如何在資料庫中執行簡單的讀取作業。</span><span class="sxs-lookup"><span data-stu-id="d688a-107">The following procedure shows how to perform a simple read operation in the database.</span></span>

### <a name="to-read-data-from-a-database"></a><span data-ttu-id="d688a-108">從資料庫讀取資料</span><span class="sxs-lookup"><span data-stu-id="d688a-108">To read data from a database</span></span>

1.  <span data-ttu-id="d688a-109">使用會話識別碼呼叫 [JetBeginTransaction](./jetbegintransaction-function.md) 或 [JetBeginTransaction2](./jetbegintransaction2-function.md) ，以啟動交易。</span><span class="sxs-lookup"><span data-stu-id="d688a-109">Call [JetBeginTransaction](./jetbegintransaction-function.md) or [JetBeginTransaction2](./jetbegintransaction2-function.md) with the session ID to start the transaction.</span></span>

2.  <span data-ttu-id="d688a-110">藉由在 *魚尾紋* 參數中使用 JET_MoveFirst 呼叫 [JetMove](./jetmove-function.md) ，將游標移到所需的記錄。</span><span class="sxs-lookup"><span data-stu-id="d688a-110">Move the cursor to the desired record by calling [JetMove](./jetmove-function.md) with JET_MoveFirst in the *cRow* parameter.</span></span> <span data-ttu-id="d688a-111">如需如何移動游標的詳細資訊，請參閱 [資料表主題中的索引](./indexing-in-the-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="d688a-111">For more information on how to move the cursor, see the [Indexing in the Table](./indexing-in-the-table.md) topic.</span></span>

3.  <span data-ttu-id="d688a-112">使用 *InfoLevel* 參數中指定的 JET_ColInfo，在目前記錄上呼叫 [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) ，以抓取資料行的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="d688a-112">Call [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) on the current record with JET_ColInfo specified in the *InfoLevel* parameter to retrieve the column ID for the column.</span></span> <span data-ttu-id="d688a-113">[JET_COLUMNDEF](./jet-columndef-structure.md)結構中會傳回資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="d688a-113">The column ID is returned in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure.</span></span>

4.  <span data-ttu-id="d688a-114">從資料行讀取資料，方法是呼叫 [JetRetrieveColumn](./jetretrievecolumn-function.md) ，並在 columnid 參數的步驟3中抓取資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="d688a-114">Read the data from the column by calling [JetRetrieveColumn](./jetretrievecolumn-function.md) with the column ID retrieved in step 3 in the columnid parameter.</span></span> <span data-ttu-id="d688a-115">*PvData* 參數包含在步驟3中所抓取 [JET_COLUMNDEF](./jet-columndef-structure.md)結構中指定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="d688a-115">The *pvData* parameter contains the type of data specified in the [JET_COLUMNDEF](./jet-columndef-structure.md) structure retrieved in step 3.</span></span>

5.  <span data-ttu-id="d688a-116">呼叫 [JetCommitTransaction](./jetcommittransaction-function.md) 將交易認可到資料庫。</span><span class="sxs-lookup"><span data-stu-id="d688a-116">Call [JetCommitTransaction](./jetcommittransaction-function.md) to commit the transaction to the database.</span></span>
