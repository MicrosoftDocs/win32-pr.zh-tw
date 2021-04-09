---
title: 使用 SetSearchPreference 方法
description: 呼叫 >idirectorysearch SetSearchPreference 方法會變更透過 >idirectorysearch 介面取得和呈現搜尋結果的方式。
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- 使用 SetSearchPreference 方法 SetSearchPreference ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 SetSearchPreference 方法
- 使用 SetSearchPreference 查詢 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020778"
---
# <a name="using-the-setsearchpreference-method"></a><span data-ttu-id="6592d-106">使用 SetSearchPreference 方法</span><span class="sxs-lookup"><span data-stu-id="6592d-106">Using the SetSearchPreference Method</span></span>

<span data-ttu-id="6592d-107">呼叫 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 方法會變更透過 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面取得和呈現搜尋結果的方式。</span><span class="sxs-lookup"><span data-stu-id="6592d-107">Calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method changes the way in which the search results are obtained and presented through the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="6592d-108">SDK 檔定義 [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6592d-108">The SDK documentation defines [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) as follows:</span></span>


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



<span data-ttu-id="6592d-109">您可以藉由傳遞陣列做為第一個參數，並將陣列大小作為第二個參數來設定多個喜好設定。</span><span class="sxs-lookup"><span data-stu-id="6592d-109">Multiple preferences may be set by passing an array as the first parameter and the array size as the second parameter.</span></span>


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



<span data-ttu-id="6592d-110">此範例會將頁面大小設定為100個數據列，並將範圍設定為 ADS \_ 範圍 \_ 子樹類型。</span><span class="sxs-lookup"><span data-stu-id="6592d-110">This example sets the page size to 100 rows and the scope to the ADS\_SCOPE\_SUBTREE type.</span></span> <span data-ttu-id="6592d-111">[頁面大小] 設定會導致伺服器在計算出100個數據列之後，立即將資料傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="6592d-111">The page size setting causes the server to immediately return data to the client, after 100 rows have been calculated.</span></span> <span data-ttu-id="6592d-112">[ADS \_ 領域] \_ 子樹設定會讓搜尋將樹狀結構中的所有分支都包含在執行搜尋的點下。</span><span class="sxs-lookup"><span data-stu-id="6592d-112">The ADS\_SCOPE\_SUBTREE setting causes the search to encompass all branches in the tree below the point from which the search is being executed.</span></span>

 

 




