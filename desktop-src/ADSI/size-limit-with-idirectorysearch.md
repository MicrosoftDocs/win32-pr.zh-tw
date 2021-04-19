---
title: 使用 >idirectorysearch 的大小限制
description: 用戶端可以專注于從伺服器傳回的少數物件，並忽略結果集的其餘部分。
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- '>idirectorysearch ADSI 的大小限制'
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、大小限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966167"
---
# <a name="size-limit-with-idirectorysearch"></a><span data-ttu-id="e306e-105">使用 >idirectorysearch 的大小限制</span><span class="sxs-lookup"><span data-stu-id="e306e-105">Size Limit with IDirectorySearch</span></span>

<span data-ttu-id="e306e-106">若要減少記憶體需求或其他目的，用戶端可以專注于從伺服器傳回的少量物件，並忽略不感興趣之結果集的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="e306e-106">To reduce the memory requirement or for other purposes, the client can focus on a small number of objects returned from the server and ignore the rest of the result set that are not of interest.</span></span> <span data-ttu-id="e306e-107">為了達成此目的，用戶端會指定搜尋大小限制和其他適當的搜尋準則。</span><span class="sxs-lookup"><span data-stu-id="e306e-107">To accomplish this, the client specifies the search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="e306e-108">例如，如果目錄儲存學校學區的測試分數，您可以藉由指定 10 (10) 和遞減排序次序的大小限制，查詢具有最高測試分數的前十名學生。</span><span class="sxs-lookup"><span data-stu-id="e306e-108">For example, if the directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten (10) and a descending sort order.</span></span>

<span data-ttu-id="e306e-109">大小限制的預設值為 [無限制]。</span><span class="sxs-lookup"><span data-stu-id="e306e-109">The default for size limit is no limit.</span></span> <span data-ttu-id="e306e-110">若要設定大小限制，請將 **ads \_ SEARCHPREF \_ 大小 \_ 限制** 搜尋選項設定為 **ADSTYPE \_ 整數** 值，其中包含傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列大小上限。</span><span class="sxs-lookup"><span data-stu-id="e306e-110">To set a size limit, set an **ADS\_SEARCHPREF\_SIZE\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the maximum size in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="e306e-111">下列程式碼範例顯示如何設定大小限制。</span><span class="sxs-lookup"><span data-stu-id="e306e-111">The following code example shows how to set the size limit.</span></span> <span data-ttu-id="e306e-112">大小限制值為零，表示沒有大小限制。</span><span class="sxs-lookup"><span data-stu-id="e306e-112">A size limit value of zero indicates no size limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="e306e-113">針對 Active Directory，大小限制會指定搜尋所要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="e306e-113">For Active Directory, the size limit specifies the maximum number of objects to be returned by the search.</span></span> <span data-ttu-id="e306e-114">此外，針對 Active Directory，搜尋所傳回的最大物件數目是1000物件。</span><span class="sxs-lookup"><span data-stu-id="e306e-114">Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.</span></span>

 

 




