---
description: 以下顯示本機查詢之 SELECT 語句的基本語法：
ms.assetid: 334aa2b9-0ef2-4a4b-9352-de5ded95afa6
title: SELECT 陳述式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e05832dab0184870a626fa4bce502d908c9b05f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980935"
---
# <a name="select-statement"></a><span data-ttu-id="4c949-103">SELECT 陳述式</span><span class="sxs-lookup"><span data-stu-id="4c949-103">SELECT Statement</span></span>

<span data-ttu-id="4c949-104">以下顯示本機查詢之 SELECT 語句的基本語法：</span><span class="sxs-lookup"><span data-stu-id="4c949-104">The following shows the basic syntax of the SELECT statement for a local query:</span></span>


```
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>] 
            
```



<span data-ttu-id="4c949-105">以下顯示 SELECT 語句語法的資料行部分：</span><span class="sxs-lookup"><span data-stu-id="4c949-105">The following shows the column portion of the SELECT statement syntax:</span></span>


```
SELECT [TOP <positive integer>] <column> [ {, <column>} ...]
```



<span data-ttu-id="4c949-106"> (s) 的資料行規范必須是有效的屬性名稱資料行，並以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="4c949-106">The column specifier(s) must be valid property name columns, separated by commas.</span></span> <span data-ttu-id="4c949-107">有效的資料行名稱是已註冊的屬性描述，或是由 Shell 的屬性系統架構定義。</span><span class="sxs-lookup"><span data-stu-id="4c949-107">Valid column names are registered property descriptions or are defined by the Shell's Property System Schema.</span></span> <span data-ttu-id="4c949-108">您只能選取在屬性系統架構中標示為可抓取的資料行。</span><span class="sxs-lookup"><span data-stu-id="4c949-108">You can select only those columns that are marked as retrievable in the Property System Schema.</span></span> <span data-ttu-id="4c949-109">如果您使用混合大小寫來識別不是系統定義屬性的屬性，則必須將資料行規范括在雙引號中。</span><span class="sxs-lookup"><span data-stu-id="4c949-109">If you use mixed case to identify properties that are not system-defined properties, you must enclose the column specifier in double quotation marks.</span></span> <span data-ttu-id="4c949-110">系統定義的屬性名稱包括以 "System" 開頭的所有屬性 (例如，) ，而且不需要引號。</span><span class="sxs-lookup"><span data-stu-id="4c949-110">System-defined property names include all properties beginning with "System" (for example, System.Contact.FirstName) and do not require quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="4c949-111">您也可以用雙引號括住系統定義的屬性名稱，以方便閱讀。</span><span class="sxs-lookup"><span data-stu-id="4c949-111">You can also enclose system-defined property names in double quotation marks for readability.</span></span> <span data-ttu-id="4c949-112">這不會影響相容性。</span><span class="sxs-lookup"><span data-stu-id="4c949-112">This does not affect compatibility.</span></span>

 

<span data-ttu-id="4c949-113">當查詢傳回的檔沒有所要求的資料行時，該檔的該資料行值就是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4c949-113">When the query returns a document that does not have the requested column, the value of that column for the document is **NULL**.</span></span>

<span data-ttu-id="4c949-114">您必須在 SELECT 語句中至少提供一個資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="4c949-114">You must provide at least one column name in a SELECT statement.</span></span> <span data-ttu-id="4c949-115">在結構化查詢語言 (SQL)  (SQL) 查詢中，您可以使用星號 (\*) 來指定要傳回資料表中的所有資料行。</span><span class="sxs-lookup"><span data-stu-id="4c949-115">In the Structured Query Language (SQL) query, you are allowed to use the asterisk (\*) to specify that all columns in a table are to be returned.</span></span> <span data-ttu-id="4c949-116">不過，沒有任何已定義且固定的屬性集會套用至所有檔。</span><span class="sxs-lookup"><span data-stu-id="4c949-116">However, no defined and fixed set of properties applies to all documents.</span></span> <span data-ttu-id="4c949-117">基於這個理由，SELECT 語句的規範中不允許 SQL 星號 <columns> 。</span><span class="sxs-lookup"><span data-stu-id="4c949-117">For this reason, the SQL asterisk is not permitted in the <columns> specifier of the SELECT statement.</span></span>

## <a name="getting-the-top-n-results"></a><span data-ttu-id="4c949-118">取得前 n 個結果</span><span class="sxs-lookup"><span data-stu-id="4c949-118">Getting the Top n Results</span></span>

<span data-ttu-id="4c949-119">您可以使用 TOP 語法來指定要傳回的結果數目上限：</span><span class="sxs-lookup"><span data-stu-id="4c949-119">You can specify a maximum number of results to return by using the TOP syntax:</span></span>


```
SELECT TOP <positive integer> <column> [ {, <column>} ...]
```



## <a name="casting-column-data-types"></a><span data-ttu-id="4c949-120">轉換資料行資料類型</span><span class="sxs-lookup"><span data-stu-id="4c949-120">Casting Column Data Types</span></span>

<span data-ttu-id="4c949-121">有時，您可能需要將從檔中解壓縮的字串資料轉換成另一種資料類型，才能進行適當的比較。</span><span class="sxs-lookup"><span data-stu-id="4c949-121">At times, you might need to cast string data extracted from documents as another data type so that an appropriate comparison can be made.</span></span> <span data-ttu-id="4c949-122">如需詳細資訊，請參閱 [轉換資料行的資料類型](-search-sql-castingdatacolumntype.md)。</span><span class="sxs-lookup"><span data-stu-id="4c949-122">For more information, refer to [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4c949-123">範例</span><span class="sxs-lookup"><span data-stu-id="4c949-123">Examples</span></span>

<span data-ttu-id="4c949-124">下列範例會傳回相符檔的名稱和 URL。</span><span class="sxs-lookup"><span data-stu-id="4c949-124">The following examples return the name and URL of matching documents.</span></span>


```
SELECT System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT TOP 10 System.ItemName, System.ItemUrl FROM SystemIndex WHERE CONTAINS('Microsoft') 
```



## <a name="related-topics"></a><span data-ttu-id="4c949-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="4c949-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4c949-126">**概念**</span><span class="sxs-lookup"><span data-stu-id="4c949-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4c949-127">轉換資料行的資料類型</span><span class="sxs-lookup"><span data-stu-id="4c949-127">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)
</dt> <dt>

<span data-ttu-id="4c949-128">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="4c949-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="4c949-129">[系統屬性](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="4c949-129">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 



