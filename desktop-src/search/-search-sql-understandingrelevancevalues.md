---
description: 在關係資料庫中，搜尋查詢所傳回的資料列必須符合查詢所呼叫的所有條件。 相反地，Windows Search 查詢可能會將符合搜尋條件的檔傳回不同的程度。
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: 瞭解相關性值
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847807"
---
# <a name="understanding-relevance-values"></a><span data-ttu-id="c46ca-104">瞭解相關性值</span><span class="sxs-lookup"><span data-stu-id="c46ca-104">Understanding Relevance Values</span></span>

<span data-ttu-id="c46ca-105">在關係資料庫中，搜尋查詢所傳回的資料列必須符合查詢所呼叫的所有條件。</span><span class="sxs-lookup"><span data-stu-id="c46ca-105">In a relational database, rows that are returned by a search query must meet all the conditions called for by the query.</span></span> <span data-ttu-id="c46ca-106">相反地，Windows Search 查詢可能會將符合搜尋條件的檔傳回不同的程度。</span><span class="sxs-lookup"><span data-stu-id="c46ca-106">In contrast, a Windows Search query can return documents that meet the search conditions to varying degrees.</span></span>

<span data-ttu-id="c46ca-107">例如，在關係資料庫中搜尋「程式」一詞，會產生包含該單字特定拼寫的記錄。</span><span class="sxs-lookup"><span data-stu-id="c46ca-107">For example, a search for the term "program" in a relational database produces records that contain that specific spelling of the word.</span></span> <span data-ttu-id="c46ca-108">記錄是否包含一或100的單字實例不會影響結果。</span><span class="sxs-lookup"><span data-stu-id="c46ca-108">Whether a record contains one or one hundred instances of the word has no impact on the results.</span></span> <span data-ttu-id="c46ca-109">相反地，Windows Search 會傳回與相符檔相關聯的關聯性值。</span><span class="sxs-lookup"><span data-stu-id="c46ca-109">In contrast, Windows Search returns a relevance value associated with the matching documents.</span></span> <span data-ttu-id="c46ca-110">標題中具有「程式」的檔相關性高於最後一個段落中只包含單字的檔。</span><span class="sxs-lookup"><span data-stu-id="c46ca-110">The relevance of documents having "program" in the title is higher than those that contain the word only in the last paragraph.</span></span> <span data-ttu-id="c46ca-111">同樣地，包含搜尋詞彙變化的檔（例如「程式」和「程式設計」）也會相符，並由查詢傳回。</span><span class="sxs-lookup"><span data-stu-id="c46ca-111">Similarly, documents containing variations of the search term, for example "programs" and "programming" also match and are returned by the query.</span></span>

<span data-ttu-id="c46ca-112">Windows Search 查詢會在名為 "rank" 的資料行中傳回整數關聯值。</span><span class="sxs-lookup"><span data-stu-id="c46ca-112">Windows Search queries return integer relevance values in the column named "rank".</span></span>

<span data-ttu-id="c46ca-113">此外：</span><span class="sxs-lookup"><span data-stu-id="c46ca-113">In addition:</span></span>

-   <span data-ttu-id="c46ca-114">查詢所傳回的排名值是介於0到1000之間的整數。</span><span class="sxs-lookup"><span data-stu-id="c46ca-114">Rank values returned by the query are integers ranging from 0 to 1000.</span></span>
-   <span data-ttu-id="c46ca-115">排名較高的值表示符合搜尋條件的檔。</span><span class="sxs-lookup"><span data-stu-id="c46ca-115">Higher rank values indicate documents that better match the search conditions.</span></span>
-   <span data-ttu-id="c46ca-116">排名值只適用于目前的查詢，因此無法在查詢之間進行比較。</span><span class="sxs-lookup"><span data-stu-id="c46ca-116">Rank values apply only to the current query, so they cannot be compared for results across queries.</span></span>
-   <span data-ttu-id="c46ca-117">排名值會相對於符合查詢的其他檔。</span><span class="sxs-lookup"><span data-stu-id="c46ca-117">Rank values are relative to the other documents matching the query.</span></span> <span data-ttu-id="c46ca-118">因此，特定檔的排名值取決於也符合查詢的其他檔。</span><span class="sxs-lookup"><span data-stu-id="c46ca-118">Therefore, the rank value of a particular document depends on the other documents that also match the query.</span></span>
-   <span data-ttu-id="c46ca-119">符合單純關聯式述詞之專案的等級值為1000。</span><span class="sxs-lookup"><span data-stu-id="c46ca-119">Rank values for items matching a purely relational predicate are 1000.</span></span>

<span data-ttu-id="c46ca-120">您可以使用 [CONTAINS](-search-sql-contains.md) 和 [FREETEXT](-search-sql-freetext.md) WHERE 子句述詞中的資料行權數，以及 rank by 子句，來操作傳回的等級值。</span><span class="sxs-lookup"><span data-stu-id="c46ca-120">You can manipulate the returned rank values by using column weights in the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) WHERE clause predicates, and the RANK BY clause.</span></span>

 

 



