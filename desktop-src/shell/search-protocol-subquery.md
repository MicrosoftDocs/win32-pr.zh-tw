---
description: 瞭解 Windows Shell 中的子查詢引數。 子查詢是一種儲存的搜尋檔案，您可以用來作為新查詢的篩選準則。
title: 'Windows Shell (的子查詢引數) '
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2d97b891-ba62-4009-bc6a-9f42e6dbbb34
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c27ce11d4d2e6ac36792f3ce47c053e9646d9903
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581596"
---
# <a name="subquery-argument-the-windows-shell"></a><span data-ttu-id="02e0e-104">Windows Shell (的子查詢引數) </span><span class="sxs-lookup"><span data-stu-id="02e0e-104">SUBQUERY Argument (The Windows Shell)</span></span>

<span data-ttu-id="02e0e-105">子查詢是已儲存的搜尋檔案 (\* . 搜尋-ms) ，您可以用來作為新查詢的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="02e0e-105">A subquery is a saved search file (\*.search-ms) that you can use as a filter for a new query.</span></span> <span data-ttu-id="02e0e-106">子查詢的結果會用來作為新查詢的來源。</span><span class="sxs-lookup"><span data-stu-id="02e0e-106">The results of the subquery are used as the source for the new query.</span></span> <span data-ttu-id="02e0e-107">例如，假設您有數個儲存的搜尋檔案，這些檔案會根據電子郵件通訊群組清單來限制查詢： mydepartment。搜尋-ms、j 和 corporatewide。搜尋-毫秒。</span><span class="sxs-lookup"><span data-stu-id="02e0e-107">For example, say you have several saved search files that restrict a query by email distribution list: mydepartment.search-ms, teamproject.search-ms, and corporatewide.search-ms.</span></span> <span data-ttu-id="02e0e-108">使用 `subquery` 引數可讓您將電子郵件搜尋限制在這些儲存的所有搜尋中。</span><span class="sxs-lookup"><span data-stu-id="02e0e-108">Using the `subquery` argument enables you to limit email searches to any or all of these saved searches.</span></span>

## <a name="example"></a><span data-ttu-id="02e0e-109">範例</span><span class="sxs-lookup"><span data-stu-id="02e0e-109">Example</span></span>


```
search:query=vacation&subquery=mydepartment.search-ms
```



### <a name="argument-information"></a><span data-ttu-id="02e0e-110">引數資訊</span><span class="sxs-lookup"><span data-stu-id="02e0e-110">Argument Information</span></span>



|                              | <span data-ttu-id="02e0e-111">值</span><span class="sxs-lookup"><span data-stu-id="02e0e-111">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="02e0e-112">**最低作業系統**</span><span class="sxs-lookup"><span data-stu-id="02e0e-112">**Minimum Operating System**</span></span> | <span data-ttu-id="02e0e-113">Windows Vista 包含 Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="02e0e-113">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



