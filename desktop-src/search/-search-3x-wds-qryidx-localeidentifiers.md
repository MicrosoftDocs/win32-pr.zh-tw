---
description: 瞭解 Windows Search 中的 inputlocale 和 keywordlocale 引數，這可協助搜尋引擎使用正確的斷詞工具。
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: '地區設定識別碼引數 (Windows Search) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403751"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="d8e75-103">地區設定識別碼引數 (Windows Search) </span><span class="sxs-lookup"><span data-stu-id="d8e75-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="d8e75-104">`inputlocale`和 `keywordlocale` 識別碼可協助搜尋引擎使用正確的斷詞工具，其方式是識別使用者輸入查詢的語言以及 Advanced Query 語法關鍵字的語言。</span><span class="sxs-lookup"><span data-stu-id="d8e75-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="d8e75-105">這些不一定是 (Lcid) 的語言代碼識別碼，因為 Windows Search 是以許多國際版本提供，而且也包含適用于其他語言的 MUI 套件。</span><span class="sxs-lookup"><span data-stu-id="d8e75-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="d8e75-106">Inputlocale 會識別使用者在中輸入其搜尋查詢之語言的 LCID，而 keywordlocale 則會識別搜尋引擎用於關鍵字的 LCID。</span><span class="sxs-lookup"><span data-stu-id="d8e75-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="d8e75-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="d8e75-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="d8e75-108">範例</span><span class="sxs-lookup"><span data-stu-id="d8e75-108">Example</span></span>](#example)
-   [<span data-ttu-id="d8e75-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8e75-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="d8e75-110">範例</span><span class="sxs-lookup"><span data-stu-id="d8e75-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="d8e75-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d8e75-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e75-112">具有 Parameter-Value 引數的開始使用</span><span class="sxs-lookup"><span data-stu-id="d8e75-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="d8e75-113">連結引數</span><span class="sxs-lookup"><span data-stu-id="d8e75-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="d8e75-114">語法引數</span><span class="sxs-lookup"><span data-stu-id="d8e75-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="d8e75-115">STACKEDBY 引數</span><span class="sxs-lookup"><span data-stu-id="d8e75-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="d8e75-116">子查詢引數</span><span class="sxs-lookup"><span data-stu-id="d8e75-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



