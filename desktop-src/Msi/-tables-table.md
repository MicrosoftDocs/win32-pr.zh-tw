---
description: '\_資料表資料表是唯讀的系統資料表，會列出資料庫中的所有資料表。 查詢此資料表，以找出資料表是否存在。'
ms.assetid: d064855b-8c10-476e-9570-cc3ab48ae998
title: _Tables 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2dc3ebafd969a07676f64f674f76c3e16ebe059
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849004"
---
# <a name="_tables-table"></a><span data-ttu-id="22fc1-104">\_資料表資料表</span><span class="sxs-lookup"><span data-stu-id="22fc1-104">\_Tables Table</span></span>

<span data-ttu-id="22fc1-105">\_資料表資料表是唯讀的系統資料表，會列出資料庫中的所有資料表。</span><span class="sxs-lookup"><span data-stu-id="22fc1-105">The \_Tables table is a read-only system table that lists all the tables in the database.</span></span> <span data-ttu-id="22fc1-106">查詢此資料表，以找出資料表是否存在。</span><span class="sxs-lookup"><span data-stu-id="22fc1-106">Query this table to find out if a table exists.</span></span>

<span data-ttu-id="22fc1-107">\_資料表資料表有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="22fc1-107">The \_Tables Table has the following column.</span></span>



| <span data-ttu-id="22fc1-108">Column</span><span class="sxs-lookup"><span data-stu-id="22fc1-108">Column</span></span> | <span data-ttu-id="22fc1-109">類型</span><span class="sxs-lookup"><span data-stu-id="22fc1-109">Type</span></span>             | <span data-ttu-id="22fc1-110">答案</span><span class="sxs-lookup"><span data-stu-id="22fc1-110">Key</span></span> | <span data-ttu-id="22fc1-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="22fc1-111">Nullable</span></span> |
|--------|------------------|-----|----------|
| <span data-ttu-id="22fc1-112">Name</span><span class="sxs-lookup"><span data-stu-id="22fc1-112">Name</span></span>   | [<span data-ttu-id="22fc1-113">Text</span><span class="sxs-lookup"><span data-stu-id="22fc1-113">Text</span></span>](text.md) | <span data-ttu-id="22fc1-114">Y</span><span class="sxs-lookup"><span data-stu-id="22fc1-114">Y</span></span>   | <span data-ttu-id="22fc1-115">N</span><span class="sxs-lookup"><span data-stu-id="22fc1-115">N</span></span>        |



 

## <a name="column"></a><span data-ttu-id="22fc1-116">Column</span><span class="sxs-lookup"><span data-stu-id="22fc1-116">Column</span></span>

<dl> <dt>

<span data-ttu-id="22fc1-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>名字</span><span class="sxs-lookup"><span data-stu-id="22fc1-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="22fc1-118">其中一個資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="22fc1-118">Name of one of the tables.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="22fc1-119">備註</span><span class="sxs-lookup"><span data-stu-id="22fc1-119">Remarks</span></span>

<span data-ttu-id="22fc1-120">因為 \_ 資料表資料表是無法透過 SQL 查詢修改的系統資料表，所以您無法使用 [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) 函數或 [**PrimaryKeys 屬性**](database-primarykeys.md)來取得主鍵。</span><span class="sxs-lookup"><span data-stu-id="22fc1-120">Because the \_Tables table is a system table that cannot be modified through SQL queries, you cannot obtain the primary keys with the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function or the [**PrimaryKeys property**](database-primarykeys.md).</span></span>

 

 



