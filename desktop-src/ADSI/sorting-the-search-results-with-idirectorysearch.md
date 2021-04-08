---
title: 使用 >idirectorysearch 排序搜尋結果
description: 依預設，搜尋結果不會以任何保證的順序傳回。 [ADS \_ SEARCHPREF \_ 排序 \_ 依據喜好設定] 會指示伺服器在指定的屬性值上排序結果集，然後再傳回給用戶端。
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch 排序搜尋結果
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、排序搜尋結果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683092"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a><span data-ttu-id="ff3f1-106">使用 >idirectorysearch 排序搜尋結果</span><span class="sxs-lookup"><span data-stu-id="ff3f1-106">Sorting the Search Results with IDirectorySearch</span></span>

<span data-ttu-id="ff3f1-107">依預設，搜尋結果不會以任何保證的順序傳回。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-107">By default, the results of a search are returned in no guaranteed order.</span></span> <span data-ttu-id="ff3f1-108">[ **ADS \_ SEARCHPREF \_ 排序 \_ 依據** 喜好設定] 會指示伺服器在指定的屬性值上排序結果集，然後再傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-108">The **ADS\_SEARCHPREF\_SORT\_ON** preference instructs the server to sort the result set on a specified attribute value before it is returned to the client.</span></span>

<span data-ttu-id="ff3f1-109">建議您將索引屬性用於排序。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-109">It is recommended that indexed attributes be used for sorting.</span></span> <span data-ttu-id="ff3f1-110">否則，伺服器必須先取得完整的結果集，並在將任何結果傳送至用戶端之前進行排序。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-110">Otherwise, the server must retrieve the complete result set and sort it before sending any results to the client.</span></span> <span data-ttu-id="ff3f1-111">這也適用于分頁搜尋。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-111">This also applies to paged searches.</span></span> <span data-ttu-id="ff3f1-112">請注意，如果篩選準則包含已編制索引的屬性，且該屬性指定為排序關鍵字，則會增加排序搜尋的效能。在此情況下，Active Directory 可在處理篩選時滿足排序。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-112">Be aware that performance of a sorted search will be increased if the filter includes an indexed attribute and that attribute is specified as the sort key; in this case, Active Directory can satisfy the sort while processing the filter.</span></span> <span data-ttu-id="ff3f1-113">例如，一組使用者的有效率排序查詢可能具有包含 (sn>smith) 的篩選準則，以及 sn 的排序關鍵字。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-113">For example, an efficient sort query for a set of users could have a filter that included (sn>smith) and a sort key of sn.</span></span>

<span data-ttu-id="ff3f1-114">使用 **ADS \_ SEARCHPREF \_ 排序 \_ 依據** 搜尋選項的伺服器端排序，將會降低伺服器的效能。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-114">Server-side sorting with the **ADS\_SEARCHPREF\_SORT\_ON** search option will reduce the performance of the server.</span></span> <span data-ttu-id="ff3f1-115">如果您將執行許多搜尋，請考慮以手動方式在用戶端上排序結果，以降低伺服器上的工作負載。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-115">If you will be performing many searches, consider sorting the results manually on the client side to reduce the workload on the server.</span></span>

<span data-ttu-id="ff3f1-116">依預設，會停用結果排序。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-116">By default, result sorting is disabled.</span></span> <span data-ttu-id="ff3f1-117">若要啟用結果排序，請針對搜尋選項設定 **ads \_ SEARCHPREF \_ 排序 \_** ，其 **ADSTYPE \_ >prov \_ 特定** 會指向 [**Ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ 分類結構**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-117">To enable result sorting, set an **ADS\_SEARCHPREF\_SORT\_ON** search option with an **ADSTYPE\_PROV\_SPECIFIC** that points to an [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="ff3f1-118">**ADS 分類 \_** 結構是用來指定要排序的屬性，以及排序的順序。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-118">The **ADS\_SORTKEY** structure is used to specify the attribute to sort on and the order of the sort.</span></span>

<span data-ttu-id="ff3f1-119">下列程式碼範例顯示如何啟用結果排序。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-119">The following code example shows how to enable result sorting.</span></span>


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



<span data-ttu-id="ff3f1-120">Active Directory 不支援針對已建立的屬性進行排序，因此無法指定用於排序的結構化屬性。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-120">Active Directory does not support sorting on constructed attributes, so it is not possible to specify a constructed attribute for sorting.</span></span> <span data-ttu-id="ff3f1-121">[**DistinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)屬性也不能用來排序。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-121">The [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) attribute also cannot be used for sorting.</span></span> <span data-ttu-id="ff3f1-122">Active Directory 也不允許在一個以上的屬性上進行排序，因此 **ads \_ SEARCHPREF \_ 排序 \_ 依據** 搜尋選項只能包含一個 [**ads 分類 \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) 結構。</span><span class="sxs-lookup"><span data-stu-id="ff3f1-122">Active Directory also does not allow sorting on more than one attribute, so the **ADS\_SEARCHPREF\_SORT\_ON** search option can only contain one [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure.</span></span>

 

 