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
# <a name="rowset-properties"></a><span data-ttu-id="89270-103">資料列集屬性</span><span class="sxs-lookup"><span data-stu-id="89270-103">Rowset Properties</span></span>

<span data-ttu-id="89270-104">從查詢傳回結果之後，您可以存取資料列集的數個屬性。</span><span class="sxs-lookup"><span data-stu-id="89270-104">After a result is returned from a query, you can access several properties for the rowset.</span></span>

<span data-ttu-id="89270-105">除了標準的 OLE DB 資料列集屬性之外，Windows Search SQL 還提供下列四個自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="89270-105">In addition to the standard OLE-DB rowset properties, Windows Search SQL offers the following four custom properties.</span></span> <span data-ttu-id="89270-106">這個屬性集的 GUID 是 {AA6EE6B0E828-11D0-B23E-00AA0047FC01}。</span><span class="sxs-lookup"><span data-stu-id="89270-106">The GUID for this property set is {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span></span>

<span data-ttu-id="89270-107">Windows Search 支援 DBPROPSET 資料列集屬性集的標準 OLE DB 屬性 DBPROP \_ COMMANDTIMEOUT。 [ \_ ](/previous-versions//ms691738(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="89270-107">Windows Search supports the standard OLE-DB property DBPROP\_COMMANDTIMEOUT of the [DBPROPSET\_ROWSET](/previous-versions//ms691738(v=vs.85)) property set.</span></span>



| <span data-ttu-id="89270-108">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="89270-108">Property name</span></span>                  | <span data-ttu-id="89270-109">PROPID/類型</span><span class="sxs-lookup"><span data-stu-id="89270-109">PROPID/type</span></span> | <span data-ttu-id="89270-110">Description</span><span class="sxs-lookup"><span data-stu-id="89270-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89270-111">DONOTCOMPUTEEXPENSIVEPROPS</span><span class="sxs-lookup"><span data-stu-id="89270-111">DONOTCOMPUTEEXPENSIVEPROPS</span></span>     | <span data-ttu-id="89270-112">15/VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="89270-112">15/VT\_BOOL</span></span> | <span data-ttu-id="89270-113">將此設定為 true，可避免在存取任何資料列集屬性時，計算昂貴的屬性，例如所找到的結果，以及需要評估整個查詢的最大排名。</span><span class="sxs-lookup"><span data-stu-id="89270-113">Setting this to true prevents computing expensive properties like Results Found and Max Rank that require evaluating the whole query when any rowset property is accessed.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="89270-114">最大排名 (最大 \_ 排名) </span><span class="sxs-lookup"><span data-stu-id="89270-114">Maximum Rank (MAX\_RANK)</span></span>       | <span data-ttu-id="89270-115">6/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="89270-115">6/VT\_I4</span></span>    | <span data-ttu-id="89270-116">針對任何結果計算的最高等級。</span><span class="sxs-lookup"><span data-stu-id="89270-116">The highest rank computed for any result.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="89270-117">找到 (結果的結果 \_) </span><span class="sxs-lookup"><span data-stu-id="89270-117">Results Found (RESULTS\_FOUND)</span></span> | <span data-ttu-id="89270-118">7/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="89270-118">7/VT\_I4</span></span>    | <span data-ttu-id="89270-119">此查詢的唯一專案總數。</span><span class="sxs-lookup"><span data-stu-id="89270-119">The total number of unique items for this query.</span></span> <span data-ttu-id="89270-120">針對 SELECT 查詢，這是資料列集中的專案數。</span><span class="sxs-lookup"><span data-stu-id="89270-120">For a SELECT query, this is the number of items in the rowset.</span></span> <span data-ttu-id="89270-121">對於查詢的群組，這是唯一分葉專案的數目。</span><span class="sxs-lookup"><span data-stu-id="89270-121">For a GROUP ON query, this is the number of unique leaf items.</span></span> <span data-ttu-id="89270-122">這個屬性不會識別最上層資料列集中的資料列數目 (最上層群組) 的數目。</span><span class="sxs-lookup"><span data-stu-id="89270-122">This property does not identify the number of rows in the top-level rowset (the number of top-level groups).</span></span>                                                        |
| <span data-ttu-id="89270-123">其中 ID (WHEREID) </span><span class="sxs-lookup"><span data-stu-id="89270-123">Where ID (WHEREID)</span></span>             | <span data-ttu-id="89270-124">8/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="89270-124">8/VT\_I4</span></span>    | <span data-ttu-id="89270-125">用於查詢之限制的識別碼。</span><span class="sxs-lookup"><span data-stu-id="89270-125">The identifier for the restrictions used for a query.</span></span> <span data-ttu-id="89270-126">如果在執行新查詢時開啟資料列集，新的查詢就可以重複使用較舊查詢中的限制，藉以充分利用已完成的工作。</span><span class="sxs-lookup"><span data-stu-id="89270-126">If a rowset is open when a new query is executed, the new query can reuse the restrictions from the older query, thereby taking advantage of the work already completed.</span></span> <span data-ttu-id="89270-127">如需重複使用 WHERE 限制的詳細資訊，請參閱 [ReuseWhere 函數](-search-sql-reusewhere.md)。</span><span class="sxs-lookup"><span data-stu-id="89270-127">For more information on reusing WHERE restrictions, refer to the [ReuseWhere function](-search-sql-reusewhere.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="89270-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="89270-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89270-129">在 Windows 7 中編制優先順序和資料列集事件的索引</span><span class="sxs-lookup"><span data-stu-id="89270-129">Indexing Prioritization and Rowset Events in Windows 7</span></span>](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
