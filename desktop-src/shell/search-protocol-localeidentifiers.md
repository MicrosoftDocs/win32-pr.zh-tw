---
description: 瞭解 Windows Shell UI 中的 inputlocale 和 keywordlocale 引數，這可協助搜尋引擎使用正確的斷詞工具。
title: " (Windows Shell 的地區設定識別碼引數) "
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 34eab39e7ed956bf68048d9ce5861c12eedbbe7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403591"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="985f3-103"> (Windows Shell 的地區設定識別碼引數) </span><span class="sxs-lookup"><span data-stu-id="985f3-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="985f3-104">`inputlocale`和 `keywordlocale` 識別碼可協助搜尋引擎使用正確的斷詞工具，其方式是識別使用者輸入查詢的語言以及 Advanced Query 語法關鍵字的語言。</span><span class="sxs-lookup"><span data-stu-id="985f3-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="985f3-105">這些不一定是 (Lcid) 的語言代碼識別碼，因為 Windows Search 是以許多國際版本提供，同時也包含多語系消費者介面 (適用于其他語言的) MUI 套件。</span><span class="sxs-lookup"><span data-stu-id="985f3-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="985f3-106">會 `inputlocale` 識別使用者在中輸入其搜尋查詢之語言的 lcid，同時 `keywordlocale` 識別搜尋引擎用於關鍵字的 lcid。</span><span class="sxs-lookup"><span data-stu-id="985f3-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="985f3-107">範例</span><span class="sxs-lookup"><span data-stu-id="985f3-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="985f3-108">引數資訊</span><span class="sxs-lookup"><span data-stu-id="985f3-108">Argument Information</span></span>



|                              | <span data-ttu-id="985f3-109">值</span><span class="sxs-lookup"><span data-stu-id="985f3-109">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="985f3-110">**最低作業系統**</span><span class="sxs-lookup"><span data-stu-id="985f3-110">**Minimum Operating System**</span></span> | <span data-ttu-id="985f3-111">Windows Vista 包含 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="985f3-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



