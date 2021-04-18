---
description: 根據 SQL-92 和 SQL-99 標準的 Microsoft Windows Search，可改善檔管理或知識管理應用程式中以檔為基礎的全文檢索搜尋。
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Microsoft Windows Search 中的 SQL 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511092"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a><span data-ttu-id="81704-103">Microsoft Windows Search 中的 SQL 擴充功能</span><span class="sxs-lookup"><span data-stu-id="81704-103">SQL Extensions in Microsoft Windows Search</span></span>

<span data-ttu-id="81704-104">根據 SQL-92 和 SQL-99 標準的 Microsoft Windows Search，可改善檔管理或知識管理應用程式中以檔為基礎的全文檢索搜尋。</span><span class="sxs-lookup"><span data-stu-id="81704-104">Microsoft Windows Search, based on the SQL-92 and SQL-99 standards, improves full-text document-based searches in document-management or knowledge-management applications.</span></span> <span data-ttu-id="81704-105">Windows Search 的改進包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="81704-105">Windows Search improvements include the following:</span></span>

## <a name="128-character-identifier-names"></a><span data-ttu-id="81704-106">128-字元識別碼名稱</span><span class="sxs-lookup"><span data-stu-id="81704-106">128-Character Identifier Names</span></span>

<span data-ttu-id="81704-107">雖然 SQL-92 和 SQL-99 會將資料行和其他識別碼限制為18個字元，但 Windows Search 支援128字元的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="81704-107">While SQL-92 and SQL-99 restrict column and other identifiers to 18 characters, Windows Search supports 128-character column names.</span></span> <span data-ttu-id="81704-108">如需詳細資訊，請參閱[識別碼](-search-sql-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="81704-108">For more information, see [Identifiers](-search-sql-identifiers.md).</span></span>

## <a name="grouping-results-by-columns"></a><span data-ttu-id="81704-109">依資料行將結果分組</span><span class="sxs-lookup"><span data-stu-id="81704-109">Grouping Results by Columns</span></span>

<span data-ttu-id="81704-110">查詢可以指定如何將結果分組。</span><span class="sxs-lookup"><span data-stu-id="81704-110">Queries can specify how to group results.</span></span> <span data-ttu-id="81704-111">您可以指定要分組的範圍，也可以指定一個以上的資料行進行分組。</span><span class="sxs-lookup"><span data-stu-id="81704-111">You can specify the ranges by which to group, and you can specify more than one column for grouping.</span></span> <span data-ttu-id="81704-112">例如，您可以將檔案大小範圍的結果群組 (大小 < 100、100 <= 大小 < 1000;1000 <= size) ，而且您可以嵌套群組。</span><span class="sxs-lookup"><span data-stu-id="81704-112">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size), and you can nest groupings.</span></span> <span data-ttu-id="81704-113">如需詳細資訊，請參閱 [群組于 .。。OVER .。。語句](-search-sql-group-on-over.md)。</span><span class="sxs-lookup"><span data-stu-id="81704-113">For more information, see [GROUP ON ... OVER... Statement](-search-sql-group-on-over.md).</span></span>

## <a name="diacritic-insensitive-searching"></a><span data-ttu-id="81704-114">Diacritic-Insensitive 搜尋</span><span class="sxs-lookup"><span data-stu-id="81704-114">Diacritic-Insensitive Searching</span></span>

<span data-ttu-id="81704-115">除了不區分大小寫的搜尋，Windows Search 支援不區分字元符號 (重音標記) 的搜尋。</span><span class="sxs-lookup"><span data-stu-id="81704-115">In addition to searching that is not case-sensitive, Windows Search supports searching that is not sensitive to diacritics (accent marks).</span></span> <span data-ttu-id="81704-116">如需詳細資訊，請參閱 [搜尋中的變音符號敏感度](-search-sql-accentinsensitivitysearches.md)。</span><span class="sxs-lookup"><span data-stu-id="81704-116">For more information, see [Diacritic Sensitivity in Searches](-search-sql-accentinsensitivitysearches.md).</span></span>

## <a name="column-weighting"></a><span data-ttu-id="81704-117">資料行加權</span><span class="sxs-lookup"><span data-stu-id="81704-117">Column Weighting</span></span>

<span data-ttu-id="81704-118">搜尋多個資料行的查詢可以指定每一個資料行的重要性。</span><span class="sxs-lookup"><span data-stu-id="81704-118">Queries that search more than one column can specify the importance of each column.</span></span> <span data-ttu-id="81704-119">[CONTAINS](-search-sql-contains.md)和[FREETEXT](-search-sql-freetext.md)述詞都支援資料行加權。</span><span class="sxs-lookup"><span data-stu-id="81704-119">The [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates both support column weighting.</span></span>

## <a name="null-predicate"></a><span data-ttu-id="81704-120">Null 述詞</span><span class="sxs-lookup"><span data-stu-id="81704-120">NULL Predicate</span></span>

<span data-ttu-id="81704-121">雖然全文檢索內容索引沒有定義的資料行集，但查詢可能需要結果集的成員進行或沒有指定的資料行。</span><span class="sxs-lookup"><span data-stu-id="81704-121">Although full-text content indexing has no defined set of columns, queries can require that members of the result set do or do not have specified columns.</span></span> <span data-ttu-id="81704-122">您無法區分檔是否有指定的屬性，並將值設定為 **Null**，而且不能有完全沒有屬性的檔。</span><span class="sxs-lookup"><span data-stu-id="81704-122">It is not possible to differentiate between a document has a specified property with the value set to **NULL**, and a document that does not have the property at all.</span></span>

## <a name="rank-modification"></a><span data-ttu-id="81704-123">排名修改</span><span class="sxs-lookup"><span data-stu-id="81704-123">Rank Modification</span></span>

<span data-ttu-id="81704-124">您 [可以使用屬性](-search-sql-understandingrelevancevalues.md) 上的權數以及屬性的別名群組，來操作搜尋結果排名。</span><span class="sxs-lookup"><span data-stu-id="81704-124">You can manipulate the search results ranking by using [weights](-search-sql-understandingrelevancevalues.md) on properties and on aliased groups of properties.</span></span> <span data-ttu-id="81704-125">排名強制型轉支援根據您指定的準則，對相關性排名進行直接操作。</span><span class="sxs-lookup"><span data-stu-id="81704-125">Rank coercion supports direct manipulation of the relevance ranking based on the criteria you specify.</span></span>

 

 



