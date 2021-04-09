---
title: 使用 >idirectorysearch 的參考追蹤
description: 參考是目錄伺服器在不包含查詢所要求之物件的足夠資料時，用來將用戶端導向至另一部伺服器的機制。
ms.assetid: ef97eafd-5227-4dd7-9f8a-6b4591261f79
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 的參考追蹤
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、參考追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fae76139dc1a68c9345cd7a7b3bb894a50a2d7b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933611"
---
# <a name="referral-chasing-with-idirectorysearch"></a><span data-ttu-id="10691-105">使用 >idirectorysearch 的參考追蹤</span><span class="sxs-lookup"><span data-stu-id="10691-105">Referral Chasing with IDirectorySearch</span></span>

<span data-ttu-id="10691-106">參考是目錄伺服器在不包含查詢所要求之物件的足夠資料時，用來將用戶端導向至另一部伺服器的機制。</span><span class="sxs-lookup"><span data-stu-id="10691-106">A referral is the mechanism that a directory server uses to direct a client to another server when it does not contain sufficient data about the object requested by a query.</span></span>

<span data-ttu-id="10691-107">在一層或子樹搜尋中，只會針對已知、立即的從屬網域、架構或設定容器傳回參考;亦即，子域是直接下階。</span><span class="sxs-lookup"><span data-stu-id="10691-107">In a one-level or subtree search, referrals are returned for known, immediately subordinate domain, schema, or configuration containers only; that is, child domains that are direct descendants.</span></span> <span data-ttu-id="10691-108">如需詳細資訊，請參閱 [搜尋範圍](/windows/desktop/AD/search-scope)。</span><span class="sxs-lookup"><span data-stu-id="10691-108">For more information, see [Search Scope](/windows/desktop/AD/search-scope).</span></span>

<span data-ttu-id="10691-109">在目錄中，並非所有資料都可在單一伺服器上使用，而是分散在網路上的數部不同伺服器上。</span><span class="sxs-lookup"><span data-stu-id="10691-109">In a directory, not all data is available on a single server, rather, it is distributed over several different servers across the network.</span></span> <span data-ttu-id="10691-110">如果伺服器共用其他伺服器可提供的資料，則可以在源伺服器上無法解析要求的查詢時，提供用戶端的參考。</span><span class="sxs-lookup"><span data-stu-id="10691-110">If the servers share the data that other servers can provide, they can provide referrals to a client when a requested query cannot be resolved on the originating server.</span></span> <span data-ttu-id="10691-111">例如，當用戶端要求伺服器 A 查詢使用者物件 (U) 時，可以建議用戶端在伺服器 B 上繼續搜尋（如果 U 不在上，但識別為 B）。用戶端可以選擇尋求參考。</span><span class="sxs-lookup"><span data-stu-id="10691-111">For example, when a client asks Server A to query a user object (U), then A can suggest that the client continue the search on Server B if U does not reside on A, but is identified to be on B. The client has the choice to pursue the referral or not.</span></span> <span data-ttu-id="10691-112">用戶端可以讓用戶端不需要擁有每一部伺服器的功能，但用戶端必須指定伺服器應該執行的參照類型。</span><span class="sxs-lookup"><span data-stu-id="10691-112">Referrals free the client from having to possess previous knowledge of the capability of each server, but the client must specify the type of referrals a server should perform.</span></span>

<span data-ttu-id="10691-113">若要啟用或停用參考追蹤，請設定 **ads \_ SEARCHPREF 「 \_ \_ 追蹤參考**」搜尋選項，其 **ADSTYPE \_ 整數** 值包含其中一個廣告會在傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中 [**\_ \_ 追蹤參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)列舉值。</span><span class="sxs-lookup"><span data-stu-id="10691-113">To enable or disable referral chasing, set an **ADS\_SEARCHPREF\_CHASE\_REFERRALS** search option with an **ADSTYPE\_INTEGER** value that contains one of the [**ADS\_CHASE\_REFERRALS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum) enumeration values in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="10691-114">下列程式碼範例示範如何啟用「查看參考」。</span><span class="sxs-lookup"><span data-stu-id="10691-114">The following code example shows how to enable chase referrals.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CHASE_REFERRALS;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = ADS_CHASE_REFERRALS_ALWAYS;
```



<span data-ttu-id="10691-115">如需 Active Directory 中參考的詳細資訊，請參閱 [參考](/windows/desktop/AD/referrals)。</span><span class="sxs-lookup"><span data-stu-id="10691-115">For more information about referrals in Active Directory, see [Referrals](/windows/desktop/AD/referrals).</span></span>

 

 