---
description: 系統資料表群組的資料表會追蹤安裝資料庫的資料表和資料行。
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: 系統資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114153"
---
# <a name="system-tables-group"></a><span data-ttu-id="ea94f-103">系統資料表群組</span><span class="sxs-lookup"><span data-stu-id="ea94f-103">System Tables Group</span></span>

<span data-ttu-id="ea94f-104">系統資料表群組的資料表會追蹤安裝資料庫的資料表和資料行。</span><span class="sxs-lookup"><span data-stu-id="ea94f-104">The tables of the system tables group track the tables and columns of the installation database.</span></span>

-   <span data-ttu-id="ea94f-105">[ \_ 資料表資料表](-tables-table.md)會追蹤資料庫中的所有資料表。</span><span class="sxs-lookup"><span data-stu-id="ea94f-105">The [\_Tables table](-tables-table.md) tracks all the tables in the database.</span></span> <span data-ttu-id="ea94f-106">這包括您可能已為自己的自訂動作建立的資料表。</span><span class="sxs-lookup"><span data-stu-id="ea94f-106">This includes tables that you may have created for your own custom actions.</span></span> <span data-ttu-id="ea94f-107">查詢此資料表，以找出資料表是否存在。</span><span class="sxs-lookup"><span data-stu-id="ea94f-107">Query this table to find out if a table exists.</span></span>
-   <span data-ttu-id="ea94f-108">[ \_ Columns 資料表](-columns-table.md)會追蹤安裝資料庫中的資料行。</span><span class="sxs-lookup"><span data-stu-id="ea94f-108">The [\_Columns table](-columns-table.md) tracks columns in the installation database.</span></span> <span data-ttu-id="ea94f-109">此資料表目前未追蹤暫存資料行。</span><span class="sxs-lookup"><span data-stu-id="ea94f-109">Temporary columns are currently not tracked by this table.</span></span> <span data-ttu-id="ea94f-110">查詢此資料表，以找出指定的資料行是否存在。</span><span class="sxs-lookup"><span data-stu-id="ea94f-110">Query this table to find out if a given column exists.</span></span>
-   <span data-ttu-id="ea94f-111">[ \_ 資料流程資料表](-streams-table.md)會列出內嵌的 OLE 資料流程。</span><span class="sxs-lookup"><span data-stu-id="ea94f-111">The [\_Streams table](-streams-table.md) lists embedded OLE data streams.</span></span>
-   <span data-ttu-id="ea94f-112">[ [ \_ 儲存體] 資料表](-storages-table.md)會列出內嵌的 OLE 資料儲存體。</span><span class="sxs-lookup"><span data-stu-id="ea94f-112">The [\_Storages table](-storages-table.md) lists embedded OLE data storages.</span></span>
-   <span data-ttu-id="ea94f-113">[ \_ 驗證資料表](-validation-table.md)。</span><span class="sxs-lookup"><span data-stu-id="ea94f-113">The [\_Validation table](-validation-table.md).</span></span> <span data-ttu-id="ea94f-114">\_驗證資料表會追蹤資料庫中每個資料行的類型和允許的範圍。</span><span class="sxs-lookup"><span data-stu-id="ea94f-114">The \_Validation table tracks the types and allowed ranges of every column in the database.</span></span> <span data-ttu-id="ea94f-115">在 \_ 資料庫驗證過程中，會使用驗證資料表來確保所有資料行都已納入考慮，而且具有正確的值。</span><span class="sxs-lookup"><span data-stu-id="ea94f-115">The \_Validation table is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="ea94f-116">此資料表並未隨附于安裝程式資料庫。</span><span class="sxs-lookup"><span data-stu-id="ea94f-116">This table is not shipped with the installer database.</span></span>

 

 



