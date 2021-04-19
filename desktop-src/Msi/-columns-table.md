---
description: '\_Columns 資料表是包含資料行目錄的唯讀系統資料表。 它會列出所有資料表的資料行。 您可以查詢此資料表，以找出指定的資料行是否存在。'
ms.assetid: 1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf
title: _Columns 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d896f330e5fc2e13b5f172581341eb11a09617d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977293"
---
# <a name="_columns-table"></a><span data-ttu-id="2452e-105">\_Columns 資料表</span><span class="sxs-lookup"><span data-stu-id="2452e-105">\_Columns Table</span></span>

<span data-ttu-id="2452e-106">\_Columns 資料表是包含資料行目錄的唯讀系統資料表。</span><span class="sxs-lookup"><span data-stu-id="2452e-106">The \_Columns table is a read-only system table that contains the column catalog.</span></span> <span data-ttu-id="2452e-107">它會列出所有資料表的資料行。</span><span class="sxs-lookup"><span data-stu-id="2452e-107">It lists the columns for all the tables.</span></span> <span data-ttu-id="2452e-108">您可以查詢此資料表，以找出指定的資料行是否存在。</span><span class="sxs-lookup"><span data-stu-id="2452e-108">You can query this table to find out if a given column exists.</span></span>

<span data-ttu-id="2452e-109">\_Columns 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="2452e-109">The \_Columns table has the following columns.</span></span>



| <span data-ttu-id="2452e-110">Column</span><span class="sxs-lookup"><span data-stu-id="2452e-110">Column</span></span> | <span data-ttu-id="2452e-111">類型</span><span class="sxs-lookup"><span data-stu-id="2452e-111">Type</span></span>                   | <span data-ttu-id="2452e-112">答案</span><span class="sxs-lookup"><span data-stu-id="2452e-112">Key</span></span> | <span data-ttu-id="2452e-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="2452e-113">Nullable</span></span> |
|--------|------------------------|-----|----------|
| <span data-ttu-id="2452e-114">資料表</span><span class="sxs-lookup"><span data-stu-id="2452e-114">Table</span></span>  | [<span data-ttu-id="2452e-115">Text</span><span class="sxs-lookup"><span data-stu-id="2452e-115">Text</span></span>](text.md)       | <span data-ttu-id="2452e-116">Y</span><span class="sxs-lookup"><span data-stu-id="2452e-116">Y</span></span>   | <span data-ttu-id="2452e-117">N</span><span class="sxs-lookup"><span data-stu-id="2452e-117">N</span></span>        |
| <span data-ttu-id="2452e-118">Number</span><span class="sxs-lookup"><span data-stu-id="2452e-118">Number</span></span> | [<span data-ttu-id="2452e-119">整數</span><span class="sxs-lookup"><span data-stu-id="2452e-119">Integer</span></span>](integer.md) | <span data-ttu-id="2452e-120">Y</span><span class="sxs-lookup"><span data-stu-id="2452e-120">Y</span></span>   | <span data-ttu-id="2452e-121">N</span><span class="sxs-lookup"><span data-stu-id="2452e-121">N</span></span>        |
| <span data-ttu-id="2452e-122">Name</span><span class="sxs-lookup"><span data-stu-id="2452e-122">Name</span></span>   | [<span data-ttu-id="2452e-123">Text</span><span class="sxs-lookup"><span data-stu-id="2452e-123">Text</span></span>](text.md)       | <span data-ttu-id="2452e-124">N</span><span class="sxs-lookup"><span data-stu-id="2452e-124">N</span></span>   | <span data-ttu-id="2452e-125">N</span><span class="sxs-lookup"><span data-stu-id="2452e-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2452e-126">資料行</span><span class="sxs-lookup"><span data-stu-id="2452e-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2452e-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>表</span><span class="sxs-lookup"><span data-stu-id="2452e-127"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="2452e-128">包含資料行之資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="2452e-128">The name of the table that contains the column.</span></span>

</dd> <dt>

<span data-ttu-id="2452e-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>數量</span><span class="sxs-lookup"><span data-stu-id="2452e-129"><span id="Number"></span><span id="number"></span><span id="NUMBER"></span>Number</span></span>
</dt> <dd>

<span data-ttu-id="2452e-130">資料表內資料行的順序。</span><span class="sxs-lookup"><span data-stu-id="2452e-130">The order of the column within the table.</span></span>

</dd> <dt>

<span data-ttu-id="2452e-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="2452e-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="2452e-132">資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="2452e-132">The name of the column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2452e-133">備註</span><span class="sxs-lookup"><span data-stu-id="2452e-133">Remarks</span></span>

<span data-ttu-id="2452e-134">因為 \_ Columns 資料表是無法透過 SQL 查詢修改的系統資料表，所以您無法使用 [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) 函數或 [**PrimaryKeys 屬性**](database-primarykeys.md)來取得主鍵。</span><span class="sxs-lookup"><span data-stu-id="2452e-134">Because the \_Columns table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

<span data-ttu-id="2452e-135">只有持續性資料行會儲存在 \_ columns 資料表中。</span><span class="sxs-lookup"><span data-stu-id="2452e-135">Only persistent columns are stored in the \_Columns table.</span></span> <span data-ttu-id="2452e-136">若要判斷暫存資料行是否存在，必須針對資料表使用 SELECT 語句來建立一個 view \* ，然後使用 MSICOLINFO NAMES 選項來迴圈處理 [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) 函式所傳回之記錄中的所有欄位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2452e-136">To determine if a temporary column exists one would need to create a view using a SELECT \* statement against the table, then loop through all fields in a record returned by the [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo) function with the MSICOLINFO\_NAMES option.</span></span>

 

 



