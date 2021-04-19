---
description: 描述 WHERE 子句或 SELECT 語句中使用的 WQL 運算子。
ms.assetid: a62de66d-d5ba-49a1-8262-bfa10ac2db75
ms.tgt_platform: multiple
title: WQL 運算子
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5cc37d03884a3609abf3f76d2c78ba22b3c9f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984206"
---
# <a name="wql-operators"></a><span data-ttu-id="e1ec6-103">WQL 運算子</span><span class="sxs-lookup"><span data-stu-id="e1ec6-103">WQL Operators</span></span>

<span data-ttu-id="e1ec6-104">Windows Management Instrumentation Query Language (WQL) 支援在 SELECT 語句的 [WHERE 子句](where-clause.md) 中使用的一組標準運算子，如下所示。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-104">The Windows Management Instrumentation Query Language (WQL) supports a set of standard operators that are used in the [WHERE clause](where-clause.md) of a SELECT statement, as follows.</span></span>



| <span data-ttu-id="e1ec6-105">運算子</span><span class="sxs-lookup"><span data-stu-id="e1ec6-105">Operator</span></span>       | <span data-ttu-id="e1ec6-106">描述</span><span class="sxs-lookup"><span data-stu-id="e1ec6-106">Description</span></span>              |
|----------------|--------------------------|
| =              | <span data-ttu-id="e1ec6-107">等於</span><span class="sxs-lookup"><span data-stu-id="e1ec6-107">Equal to</span></span>                 |
| <           | <span data-ttu-id="e1ec6-108">小於</span><span class="sxs-lookup"><span data-stu-id="e1ec6-108">Less than</span></span>                |
| >           | <span data-ttu-id="e1ec6-109">大於</span><span class="sxs-lookup"><span data-stu-id="e1ec6-109">Greater than</span></span>             |
| <=          | <span data-ttu-id="e1ec6-110">小於或等於</span><span class="sxs-lookup"><span data-stu-id="e1ec6-110">Less than or equal to</span></span>    |
| >=          | <span data-ttu-id="e1ec6-111">大於或等於</span><span class="sxs-lookup"><span data-stu-id="e1ec6-111">Greater than or equal to</span></span> |
| <span data-ttu-id="e1ec6-112">！ = 或 <></span><span class="sxs-lookup"><span data-stu-id="e1ec6-112">!= or <></span></span> | <span data-ttu-id="e1ec6-113">不等於</span><span class="sxs-lookup"><span data-stu-id="e1ec6-113">Not equal to</span></span>             |



 

<span data-ttu-id="e1ec6-114">有幾個額外的 WQL 特定運算子：是、不是、ISA 和 LIKE。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-114">There are a few additional WQL-specific operators: IS, IS NOT, ISA, and LIKE.</span></span> <span data-ttu-id="e1ec6-115">只有當常數是 **Null** 時，才會在 WHERE 子句中有效，而不是運算子。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-115">The IS and IS NOT operators are valid in the WHERE clause only if the constant is **NULL**.</span></span> <span data-ttu-id="e1ec6-116">例如，下列查詢是有效的：</span><span class="sxs-lookup"><span data-stu-id="e1ec6-116">For example, the following queries are valid:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NULL
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT NULL
```



<span data-ttu-id="e1ec6-117">下列查詢顯示的無效用法為，而且不是：</span><span class="sxs-lookup"><span data-stu-id="e1ec6-117">The following queries show invalid uses of IS and IS NOT:</span></span>


```sql
SELECT * FROM Win32_LogicalDisk WHERE DriveType IS 5
SELECT * FROM Win32_LogicalDisk WHERE FileSystem IS NOT "NTFS"
```



<span data-ttu-id="e1ec6-118">ISA 運算子用於資料和事件查詢的 WHERE 子句中，用來測試類別階層的内嵌物件。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-118">The ISA operator is used in the WHERE clause of data and event queries to test embedded objects for a class hierarchy.</span></span> <span data-ttu-id="e1ec6-119">ISA 運算子在要求類別階層時，不需要追蹤新衍生的類別。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-119">The ISA operator eliminates the need for keeping track of newly derived classes when requesting a hierarchy of classes.</span></span> <span data-ttu-id="e1ec6-120">當您使用 ISA 時，所要求類別的新建立和現有子類別會自動包含在結果集中。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-120">When you use ISA, newly created and existing subclasses of the requested class are automatically included in the result set.</span></span>

<span data-ttu-id="e1ec6-121">如需此運算子的語法和用法的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="e1ec6-121">For more information about the syntax and use of this operator, see the following topics:</span></span>

-   [<span data-ttu-id="e1ec6-122">資料查詢的 ISA 運算子</span><span class="sxs-lookup"><span data-stu-id="e1ec6-122">ISA Operator for Data Queries</span></span>](isa-operator-for-data-queries.md)
-   [<span data-ttu-id="e1ec6-123">事件查詢的 ISA 運算子</span><span class="sxs-lookup"><span data-stu-id="e1ec6-123">ISA Operator for Event Queries</span></span>](isa-operator-for-event-queries.md)
-   [<span data-ttu-id="e1ec6-124">適用于架構查詢的 ISA 運算子</span><span class="sxs-lookup"><span data-stu-id="e1ec6-124">ISA Operator for Schema Queries</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="e1ec6-125">LIKE 運算子在 WHERE 子句中是有效的，用來判斷指定的字元字串是否符合指定的模式。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-125">The LIKE operator is valid in the WHERE clause and is used to determine whether a given character string matches a specified pattern.</span></span> <span data-ttu-id="e1ec6-126">例如，下列查詢會傳回 Win32 類別的所有實例 \_ 。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-126">For example, the following query returns all instances of Win32\_ classes.</span></span>


```sql
SELECT * FROM Meta_Class WHERE __Class LIKE "%Win32%"
```



<span data-ttu-id="e1ec6-127">如需這個運算子的語法和用法的詳細資訊，請參閱 [LIKE 運算子](like-operator.md)。</span><span class="sxs-lookup"><span data-stu-id="e1ec6-127">For more information about the syntax and use of this operator, see [LIKE Operator](like-operator.md).</span></span>

 

 



