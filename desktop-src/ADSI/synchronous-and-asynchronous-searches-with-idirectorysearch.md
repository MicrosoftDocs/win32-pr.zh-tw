---
title: 使用 >idirectorysearch 進行同步和非同步搜尋
description: 當您使用 >idirectorysearch 介面執行搜尋時，>idirectorysearch ExecuteSearch 方法不會將搜尋要求傳送至伺服器。
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 進行同步和非同步搜尋
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、同步和非同步搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371835"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a><span data-ttu-id="b3cbc-105">使用 >idirectorysearch 進行同步和非同步搜尋</span><span class="sxs-lookup"><span data-stu-id="b3cbc-105">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>

<span data-ttu-id="b3cbc-106">當您使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面執行搜尋時， [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 方法不會將搜尋要求傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-106">When you perform a search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method does not send the search request to the server.</span></span> <span data-ttu-id="b3cbc-107">這個方法只會儲存搜尋參數。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-107">This method only saves the search parameters.</span></span> <span data-ttu-id="b3cbc-108">當您呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) 或 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)時，會實際傳送搜尋要求。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-108">The search request is actually sent when you call [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span></span>

<span data-ttu-id="b3cbc-109">針對 Active Directory 搜尋，同步與非同步之間的主要差異在於傳回結果的第一個資料列，也就是當第一個 [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) 或 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 呼叫傳回時。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-109">For Active Directory searches, the primary difference between synchronous and asynchronous is when the first row of the result is returned, that is, when the first [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) call returns.</span></span>

<span data-ttu-id="b3cbc-110">在同步搜尋中，如果未啟用分頁功能，當伺服器已經建立並將整個結果集傳回給用戶端時，就會傳回第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-110">In a synchronous search, if paging is not enabled, the first row is returned when the server has constructed and returned the entire result set to the client.</span></span> <span data-ttu-id="b3cbc-111">如果啟用分頁，則傳回結果集的第一個頁面時，就會傳回第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-111">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="b3cbc-112">在非同步搜尋中，如果未啟用分頁功能，當伺服器已經建立結果集的第一個資料列時，就會傳回第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-112">In an asynchronous search, if paging is not enabled, the first row is returned when the server has constructed the first row of the result set.</span></span> <span data-ttu-id="b3cbc-113">如果啟用分頁，則傳回結果集的第一個頁面時，就會傳回第一個資料列。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-113">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="b3cbc-114">預設搜尋類型為同步。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-114">The default search type is synchronous.</span></span> <span data-ttu-id="b3cbc-115">若要指定非同步搜尋，請在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，設定 **\_ SEARCHPREF \_ 非同步** 搜尋選項 **ADSTYPE \_ 布林** 值為 **TRUE** 的 ads。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-115">To specify an asynchronous search, set an **ADS\_SEARCHPREF\_ASYNCHRONOUS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="b3cbc-116">下列程式碼範例會顯示這項作業。</span><span class="sxs-lookup"><span data-stu-id="b3cbc-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




