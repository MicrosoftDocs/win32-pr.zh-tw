---
description: 深入瞭解：將資料表加入至資料庫
title: 將資料表加入至資料庫
TOCTitle: Adding Tables to the Database
ms:assetid: 176d4fea-c856-441b-bd58-165b37c35095
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269195(v=EXCHG.10)
ms:contentKeyID: 32765498
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 67569f8efc164cc7156f346b6754f13b296d3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936573"
---
# <a name="adding-tables-to-the-database"></a><span data-ttu-id="a1fd9-103">將資料表加入至資料庫</span><span class="sxs-lookup"><span data-stu-id="a1fd9-103">Adding Tables to the Database</span></span>


<span data-ttu-id="a1fd9-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="a1fd9-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="adding-tables-to-the-database"></a><span data-ttu-id="a1fd9-105">將資料表加入至資料庫</span><span class="sxs-lookup"><span data-stu-id="a1fd9-105">Adding Tables to the Database</span></span>

<span data-ttu-id="a1fd9-106">資料表是一組異類記錄，這些記錄會以實體和邏輯方式將資料庫中的資料分組。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-106">Tables are a heterogeneous collection of records that physically and logically group the data in the database.</span></span> <span data-ttu-id="a1fd9-107">資料表是由其名稱唯一識別。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-107">Tables are uniquely identified by their name.</span></span> <span data-ttu-id="a1fd9-108">資料表識別碼 ([JET_TABLEID](./jet-tableid.md)) 是資料指標的控制碼，可用來更新和流覽資料表。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-108">The table ID ([JET_TABLEID](./jet-tableid.md)) is a handle to a cursor that is used to update and navigate tables.</span></span> <span data-ttu-id="a1fd9-109">您可以在相同的資料表上開啟多個 [JET_TABLEID](./jet-tableid.md) 。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-109">You may open multiple [JET_TABLEID](./jet-tableid.md) on the same table.</span></span>

<span data-ttu-id="a1fd9-110">現有的資料表會在 [JetOpenTable](./jetopentable-function.md)的呼叫中開啟，而且會建立新的資料表，而不會有 [JetCreateTable](./jetcreatetable-function.md)的資料列或資料行。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-110">An existing table is opened in the call to [JetOpenTable](./jetopentable-function.md), and a new table is created without rows or columns with [JetCreateTable](./jetcreatetable-function.md).</span></span> <span data-ttu-id="a1fd9-111">若要以自動方式建立一組初始的資料行和索引的資料表，請呼叫 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) 或 [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-111">To atomically create a table with an initial set of columns and indices, call [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md) or [JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md).</span></span> <span data-ttu-id="a1fd9-112">資料表的初始大小是在 [JetCreateTable](./jetcreatetable-function.md)的 *lPages* 參數中指定，或是呼叫 [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)中的 [JET_TABLECREATE](./jet-tablecreate-structure.md)結構的 **ulPages** 成員提供。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-112">The initial size of the table is given in the *lPages* parameter in [JetCreateTable](./jetcreatetable-function.md) or the **ulPages** member of the [JET_TABLECREATE](./jet-tablecreate-structure.md) structure in the call to [JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md).</span></span> <span data-ttu-id="a1fd9-113">將資料加入資料表時，資料表會自動成長。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-113">Tables grow automatically when data is added to the table.</span></span> <span data-ttu-id="a1fd9-114">成長與資料表的初始大小成正比。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-114">The growth is proportional to the initial size of the table.</span></span> <span data-ttu-id="a1fd9-115">您可以使用 [JetAddColumn](./jetaddcolumn-function.md)隨時將資料行加入至資料表。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-115">Columns may be added to the table at any time with [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="a1fd9-116">當應用程式不再需要存取資料表時，可以使用 [JetCloseTable](./jetclosetable-function.md)來關閉資料指標。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-116">When the application no longer needs to access the table, the cursor can be closed with [JetCloseTable](./jetclosetable-function.md).</span></span> <span data-ttu-id="a1fd9-117">您可以透過呼叫 [JetDeleteTable](./jetdeletetable-function.md)來刪除資料表。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-117">The table may be deleted via a call to [JetDeleteTable](./jetdeletetable-function.md).</span></span>

<span data-ttu-id="a1fd9-118">資料表作業應該在交易內容中執行。</span><span class="sxs-lookup"><span data-stu-id="a1fd9-118">Table operations should be performed within the context of a transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1fd9-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1fd9-119">See Also</span></span>

[<span data-ttu-id="a1fd9-120">交易</span><span class="sxs-lookup"><span data-stu-id="a1fd9-120">Transactions</span></span>](./transactions.md)
