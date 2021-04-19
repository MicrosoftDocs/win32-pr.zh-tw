---
description: 在 SELECT 語句之後，您可以使用 FROM 子句來指定搜尋相符檔的位置。
ms.assetid: 437d36d1-dd6d-4405-8f35-c37fd04fa0f6
title: FROM 子句
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37100a614ca7cc08cdf510f27e42b045acc1ec23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970381"
---
# <a name="from-clause"></a><span data-ttu-id="22da2-103">FROM 子句</span><span class="sxs-lookup"><span data-stu-id="22da2-103">FROM Clause</span></span>

<span data-ttu-id="22da2-104">在 SELECT 語句之後，您可以使用 FROM 子句來指定搜尋相符檔的位置。</span><span class="sxs-lookup"><span data-stu-id="22da2-104">Following the SELECT statement, you use the FROM clause to specify where to search for matching documents.</span></span> <span data-ttu-id="22da2-105">以下是本機查詢之 FROM 子句的語法：</span><span class="sxs-lookup"><span data-stu-id="22da2-105">The following is the syntax of the FROM clause for a local query:</span></span>


```
FROM [<ComputerName>.]SystemIndex
```



<span data-ttu-id="22da2-106">Windows Search 目前僅支援一個目錄 SystemIndex。</span><span class="sxs-lookup"><span data-stu-id="22da2-106">Currently, Windows Search supports only one catalog, SystemIndex.</span></span> <span data-ttu-id="22da2-107">若要查詢遠端電腦的本機目錄，請在類別目錄和目錄子句中的遠端電腦上，將電腦名稱稱包含在目錄之前，以及通用命名慣例 (UNC) 路徑。</span><span class="sxs-lookup"><span data-stu-id="22da2-107">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

<span data-ttu-id="22da2-108">您可以在 WHERE 子句中指定範圍做為限制，如 [範圍和目錄](-search-sql-folderdepth.md) 述詞主題所述。</span><span class="sxs-lookup"><span data-stu-id="22da2-108">You specify a scope as a restriction in the WHERE clause, as described in the [SCOPE and DIRECTORY Predicates](-search-sql-folderdepth.md) topic.</span></span>

## <a name="examples"></a><span data-ttu-id="22da2-109">範例</span><span class="sxs-lookup"><span data-stu-id="22da2-109">Examples</span></span>


```
SELECT System.ItemName,System.ItemUrl
FROM SystemIndex WHERE CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM zarascomputer.SystemIndex WHERE SCOPE='file://zarascomputer/SomeFolder' AND CONTAINS('Microsoft')

SELECT System.Author,System.ItemName,System.ItemUrl
FROM server.SystemIndex WHERE SCOPE='file://server/users' AND CONTAINS('Microsoft')
```



<span data-ttu-id="22da2-110">在上述範例的第二個範例中，查詢會以名為 "zarascomputer" 的遠端電腦為目標。</span><span class="sxs-lookup"><span data-stu-id="22da2-110">In the second of the preceding examples, the query targets a remote computer called "zarascomputer".</span></span> <span data-ttu-id="22da2-111">請注意，此電腦名稱稱同時出現在 FROM 和 SCOPE 子句中。</span><span class="sxs-lookup"><span data-stu-id="22da2-111">Notice that this computer name appears in both the FROM and SCOPE clauses.</span></span> <span data-ttu-id="22da2-112">在第三個範例中，查詢會以名為 "server" 的伺服器上的共用名稱 "users" 為目標， (其中 UNC 路徑會是 \\ \\ 伺服器 \\ 使用者) 。</span><span class="sxs-lookup"><span data-stu-id="22da2-112">In the third example, the query targets a share name "users" on a server named "server" (where the UNC path would be \\\\server\\users).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22da2-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="22da2-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="22da2-114">**參考**</span><span class="sxs-lookup"><span data-stu-id="22da2-114">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="22da2-115">搜尋 SQL 語法總覽</span><span class="sxs-lookup"><span data-stu-id="22da2-115">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="22da2-116">SELECT 語句</span><span class="sxs-lookup"><span data-stu-id="22da2-116">SELECT Statement</span></span>](-search-sql-select.md)
</dt> <dt>

[<span data-ttu-id="22da2-117">WHERE 子句</span><span class="sxs-lookup"><span data-stu-id="22da2-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="22da2-118">範圍和目錄述詞</span><span class="sxs-lookup"><span data-stu-id="22da2-118">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> </dl>

 

 



