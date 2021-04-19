---
title: 使用 >idirectorysearch 只傳回屬性名稱
description: 您可以執行搜尋來判斷特定物件可使用的資料類型。
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch ADSI 只傳回屬性名稱
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、只傳回屬性名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966778"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a><span data-ttu-id="e868c-105">使用 >idirectorysearch 只傳回屬性名稱</span><span class="sxs-lookup"><span data-stu-id="e868c-105">Returning Only Attribute Names with IDirectorySearch</span></span>

<span data-ttu-id="e868c-106">您可以執行搜尋來判斷特定物件可使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="e868c-106">You can perform a search to determine what type of data is available for a particular object.</span></span> <span data-ttu-id="e868c-107">在此情況下，您只會對屬性名稱感興趣，而不是物件的屬性值。</span><span class="sxs-lookup"><span data-stu-id="e868c-107">In this case, you are only interested in the attributes names, not the attribute values of the object.</span></span> <span data-ttu-id="e868c-108">**ADS \_ SEARCHPREF \_ \_ 僅 ATTRIBTYPES** 選項會導致伺服器只傳回屬性名稱，而不會傳回屬性值。</span><span class="sxs-lookup"><span data-stu-id="e868c-108">The **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option causes the server to only return the attribute names and not the attribute values.</span></span> <span data-ttu-id="e868c-109">不過，結果集會包含已指派值的屬性。</span><span class="sxs-lookup"><span data-stu-id="e868c-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="e868c-110">例如，請考慮具有下列屬性的物件：</span><span class="sxs-lookup"><span data-stu-id="e868c-110">For example, consider an object with the following attributes:</span></span>

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

<span data-ttu-id="e868c-111">當設定 **ADS \_ SEARCHPREF \_ \_ 僅 ATTRIBTYPES** 選項時，結果集會包含：</span><span class="sxs-lookup"><span data-stu-id="e868c-111">When the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option is set, the result set includes:</span></span>

``` syntax
name
sn
department
phone
```

<span data-ttu-id="e868c-112">預設值是要傳回的屬性值和名稱。</span><span class="sxs-lookup"><span data-stu-id="e868c-112">The default is for both attribute values and names to be returned.</span></span>

<span data-ttu-id="e868c-113">若只要抓取屬性名稱，請在傳遞至 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列中，將 [ **\_ \_ \_ 僅限 SEARCHPREF ATTRIBTYPES** ] 搜尋選項設定為 [ **TRUE** ] **ADSTYPE \_ 布林** 值。</span><span class="sxs-lookup"><span data-stu-id="e868c-113">To retrieve only attribute names, set an **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="e868c-114">下列程式碼範例示範如何只取得屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="e868c-114">The following code example shows how to retrieve attribute names only.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



<span data-ttu-id="e868c-115">如需詳細資訊和示範如何使用 **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** 搜尋選項的程式碼範例，請參閱 [搜尋屬性的範例程式碼](example-code-for-searching-for-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="e868c-115">For more information and a code example that shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option, see [Example Code for Searching for Attributes](example-code-for-searching-for-attributes.md).</span></span>

 

 




