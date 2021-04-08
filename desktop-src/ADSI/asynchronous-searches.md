---
title: 非同步搜尋
description: 在 GetFirstRow 的呼叫中啟用非同步 (非同步) 搜尋結果，或在從伺服器傳回第一個專案之前，先呼叫 GetNextRow 區塊。
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- 非同步搜尋 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931858"
---
# <a name="asynchronous-searches"></a><span data-ttu-id="dab16-104">非同步搜尋</span><span class="sxs-lookup"><span data-stu-id="dab16-104">Asynchronous Searches</span></span>

<span data-ttu-id="dab16-105">在 **GetFirstRow** 的呼叫中啟用非同步 (非同步) 搜尋結果，或在從伺服器傳回第一個專案之前，先呼叫 **GetNextRow** 區塊。</span><span class="sxs-lookup"><span data-stu-id="dab16-105">Enabling asynchronous (async) search results in a call to **GetFirstRow** or the first call to **GetNextRow** blocks until the first entry is returned from the server.</span></span> <span data-ttu-id="dab16-106">也就是說，如果伺服器上的搜尋需要很長的時間，則會快速傳回前幾個結果。</span><span class="sxs-lookup"><span data-stu-id="dab16-106">That is, if the search on the server requires much time, the first few results are returned quickly.</span></span> <span data-ttu-id="dab16-107">使用搜尋結果填入清單方塊時，這會有所説明。</span><span class="sxs-lookup"><span data-stu-id="dab16-107">This can help when populating a list box with search results.</span></span> <span data-ttu-id="dab16-108">搜尋結果會在傳回時顯示。</span><span class="sxs-lookup"><span data-stu-id="dab16-108">Search results are displayed as they are returned.</span></span>

<span data-ttu-id="dab16-109">如果已停用 async，則第一次呼叫 **GetFirstRow** 或 **GetNextRow** 將會封鎖，直到伺服器計算整個結果集並傳回為止。</span><span class="sxs-lookup"><span data-stu-id="dab16-109">If async is disabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server computes the entire result set and returns.</span></span> <span data-ttu-id="dab16-110">只有傳回的第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="dab16-110">Only then is the first row returned.</span></span> <span data-ttu-id="dab16-111">如果預期結果集很大，則不建議這樣做。</span><span class="sxs-lookup"><span data-stu-id="dab16-111">This is not recommended if the result set is expected to be large.</span></span>

<span data-ttu-id="dab16-112">如果同時啟用分頁和非同步，則第一次對 **GetFirstRow** 或 **GetNextRow** 的呼叫將會封鎖，直到伺服器產生並傳送結果的第一頁為止。</span><span class="sxs-lookup"><span data-stu-id="dab16-112">If both paging and async are enabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server generates and sends the first page of results.</span></span> <span data-ttu-id="dab16-113">如果設定合理的頁面大小，則會立即顯示結果。</span><span class="sxs-lookup"><span data-stu-id="dab16-113">If a reasonable page size was set, results will appear immediately.</span></span> <span data-ttu-id="dab16-114">更重要的是，如果搜尋結果預期會很大，而且您搜尋特定的專案，就不需要在找出您感興趣的專案之後，從伺服器要求更多結果。</span><span class="sxs-lookup"><span data-stu-id="dab16-114">More importantly, if the search results are expected to be very large, and you search for a particular entry, it is not required that you request more results from the server after you have found the entries that interest you.</span></span>

<span data-ttu-id="dab16-115">分頁的非同步搜尋提供搜尋的精確控制。</span><span class="sxs-lookup"><span data-stu-id="dab16-115">A paged async search provides fine control of a search.</span></span> <span data-ttu-id="dab16-116">如果搜尋結果可能很大，而且需要從伺服器大量時間，這就很有用。</span><span class="sxs-lookup"><span data-stu-id="dab16-116">This is useful if the search results may be very large and require extensive time from the server.</span></span>

<span data-ttu-id="dab16-117">如需有關使用非同步搜尋與特定搜尋介面的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="dab16-117">For more information about using asynchronous searches with a specific search interface, see:</span></span>

-   [<span data-ttu-id="dab16-118">使用 >idirectorysearch 進行同步和非同步搜尋</span><span class="sxs-lookup"><span data-stu-id="dab16-118">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="dab16-119">使用 ActiveX Data Objects 搜尋</span><span class="sxs-lookup"><span data-stu-id="dab16-119">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="dab16-120">使用 OLE DB 搜尋</span><span class="sxs-lookup"><span data-stu-id="dab16-120">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




