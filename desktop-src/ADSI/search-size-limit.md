---
title: 搜尋大小限制
description: 若要減少記憶體需求，用戶端可以專注于從伺服器傳回的少數物件，並忽略結果集的其餘部分。
ms.assetid: 675a4931-dfa4-4948-936b-dee27add530c
ms.tgt_platform: multiple
keywords:
- 搜尋大小限制 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd11148f9e887df1e15e221e8188f9e9e3b10d33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931828"
---
# <a name="search-size-limit"></a><span data-ttu-id="d89e7-104">搜尋大小限制</span><span class="sxs-lookup"><span data-stu-id="d89e7-104">Search Size Limit</span></span>

<span data-ttu-id="d89e7-105">若要減少記憶體需求，用戶端可以專注于從伺服器傳回的少數物件，並忽略結果集的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="d89e7-105">To reduce memory requirements, a client can focus on a small number of objects returned from the server and ignore the rest of the result set.</span></span> <span data-ttu-id="d89e7-106">為了達成此目的，用戶端會指定搜尋大小限制和其他適當的搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="d89e7-106">To accomplish this, the client specifies a search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="d89e7-107">例如，如果目錄儲存學校學區的測試分數，您可以藉由指定10和遞減排序次序的大小限制，查詢具有最高測試分數的前十名學生。</span><span class="sxs-lookup"><span data-stu-id="d89e7-107">For example, if a directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten and a descending sort order.</span></span>

<span data-ttu-id="d89e7-108">如需有關搭配特定搜尋介面使用 [搜尋大小限制] 選項的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="d89e7-108">For more information about using the search size limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="d89e7-109">使用 >idirectorysearch 的大小限制</span><span class="sxs-lookup"><span data-stu-id="d89e7-109">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="d89e7-110">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="d89e7-110">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="d89e7-111">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="d89e7-111">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




