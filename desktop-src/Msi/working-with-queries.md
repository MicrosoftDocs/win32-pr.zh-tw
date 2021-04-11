---
description: 因為安裝程式使用關係資料庫，所以有一些函數可讓結構化查詢語言 (SQL)  (SQL) 查詢到資料庫。 下列程式描述如何使用 SQL 來查詢資料庫。
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: 使用查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944472"
---
# <a name="working-with-queries"></a><span data-ttu-id="51bb8-104">使用查詢</span><span class="sxs-lookup"><span data-stu-id="51bb8-104">Working with Queries</span></span>

<span data-ttu-id="51bb8-105">因為安裝程式使用關係資料庫，所以有一些函數可讓結構化查詢語言 (SQL)  (SQL) 查詢到資料庫。</span><span class="sxs-lookup"><span data-stu-id="51bb8-105">Because the installer uses a relational database, there are functions for making Structured Query Language (SQL) queries to the database.</span></span> <span data-ttu-id="51bb8-106">下列程式描述如何使用 SQL 來查詢資料庫。</span><span class="sxs-lookup"><span data-stu-id="51bb8-106">The following procedure describes how to use SQL to query a database.</span></span>

<span data-ttu-id="51bb8-107">**若要使用 SQL 查詢資料庫**</span><span class="sxs-lookup"><span data-stu-id="51bb8-107">**To query a database with SQL**</span></span>

1.  <span data-ttu-id="51bb8-108">藉由呼叫 [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)函數，以適當的 SQL 語句開啟 [**View**](view-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="51bb8-108">Open the [**View**](view-object.md) object, with the appropriate SQL statement, by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>

    <span data-ttu-id="51bb8-109">[**View**](view-object.md)物件是將查詢套用至一組資料表所建立的邏輯資料表。</span><span class="sxs-lookup"><span data-stu-id="51bb8-109">A [**View**](view-object.md) object is the logical table created by applying a query to a set of tables.</span></span> <span data-ttu-id="51bb8-110">SQL 查詢必須遵守安裝程式所提供的 [sql 語法](sql-syntax.md) 。</span><span class="sxs-lookup"><span data-stu-id="51bb8-110">SQL queries must adhere to the [SQL syntax](sql-syntax.md) provided by the installer.</span></span> <span data-ttu-id="51bb8-111">此 SQL 語句可以包含在 **View** 物件執行之前未指定的參數標記。</span><span class="sxs-lookup"><span data-stu-id="51bb8-111">This SQL statement can contain parameter markers that are not specified until the **View** object runs.</span></span>

2.  <span data-ttu-id="51bb8-112">藉由呼叫 [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)函數來執行 [**View**](view-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="51bb8-112">Run the [**View**](view-object.md) object by calling the [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) function.</span></span>
3.  <span data-ttu-id="51bb8-113">藉由呼叫 [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)函式，從 [**View**](view-object.md)物件取出下一筆記錄。</span><span class="sxs-lookup"><span data-stu-id="51bb8-113">Retrieve the next record from a [**View**](view-object.md) object by calling the [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) function.</span></span>
4.  <span data-ttu-id="51bb8-114">藉由呼叫 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)函數來修改 [**View**](view-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="51bb8-114">Modify the [**View**](view-object.md) object by calling the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span>

    <span data-ttu-id="51bb8-115">您也可以藉由傳遞適當的旗標，以 [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) 驗證資料。</span><span class="sxs-lookup"><span data-stu-id="51bb8-115">You can also validate data with [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) by passing the appropriate flags.</span></span> <span data-ttu-id="51bb8-116">如果 **MsiViewModify** \_ 從驗證要求傳回錯誤的 \_ 資料無效，則基礎資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="51bb8-116">If **MsiViewModify** returns ERROR\_INVALID\_DATA from a validation request, the underlying data is corrupt.</span></span>

5.  <span data-ttu-id="51bb8-117">藉由呼叫 [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)函數，取得 [**View**](view-object.md)物件的詳細錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="51bb8-117">Obtain detailed error information on the [**View**](view-object.md) object by calling the [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) function.</span></span>
6.  <span data-ttu-id="51bb8-118">藉由呼叫 [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)函數來關閉 [**View**](view-object.md)物件。</span><span class="sxs-lookup"><span data-stu-id="51bb8-118">Close the [**View**](view-object.md) object by calling the [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) function.</span></span>

<span data-ttu-id="51bb8-119">如需詳細資訊，請參閱 [使用 SQL 和腳本的資料庫查詢範例](examples-of-database-queries-using-sql-and-script.md)。</span><span class="sxs-lookup"><span data-stu-id="51bb8-119">For more information, see [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

 

 



