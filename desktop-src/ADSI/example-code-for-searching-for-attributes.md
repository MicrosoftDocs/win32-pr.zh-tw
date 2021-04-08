---
title: 用於搜尋屬性的範例程式碼
description: 下列程式碼範例示範如何使用 ADS \_ SEARCHPREF \_ \_ 僅 ATTRIBTYPES 搜尋喜好設定，只取出已指派值的屬性名稱。
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI，範例程式碼 C/c + +，搜尋屬性
- 用於搜尋屬性的範例程式碼
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、只傳回屬性名稱、範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344ce99fe9de606212d786ff2e7b88b5eba34d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671155"
---
# <a name="example-code-for-searching-for-attributes"></a><span data-ttu-id="960ce-106">用於搜尋屬性的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="960ce-106">Example Code for Searching for Attributes</span></span>

<span data-ttu-id="960ce-107">下列程式碼範例示範如何使用 **ADS \_ SEARCHPREF \_ \_ 僅 ATTRIBTYPES** 搜尋喜好設定，只取出已指派值的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="960ce-107">The following code example shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search preference to retrieve only the names of attributes to which values have been assigned.</span></span> <span data-ttu-id="960ce-108">此範例會初始化 [**ADS \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)結構，並透過呼叫 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面的 [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法來設定搜尋喜好設定。</span><span class="sxs-lookup"><span data-stu-id="960ce-108">The example initializes an [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structure and sets the search preference by calling the [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method of the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="960ce-109">然後，此範例會呼叫 [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 方法來執行搜尋。</span><span class="sxs-lookup"><span data-stu-id="960ce-109">The example then calls the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method to perform the search.</span></span>


```C++
// Setting the search preference.
// m_pSearch is a valid pointer to an IDirectorySearch interface.
ADS_SEARCHPREF_INFO prefInfo[1];
LPWSTR pszColumn = NULL;

// Set the search preference to indicate attribute names only.
prefInfo[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
prefInfo[0].vValue.dwType = ADSTYPE_BOOLEAN;
prefInfo[0].vValue.Integer = TRUE;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);

// Execute the search.
hr = m_pSearch->ExecuteSearch(
                L"(|(objectCategory=domainDNS)(objectCategory=organizationalUnit))", 
                NULL, -1, &hSearch );

if(FAILED(hr))
{
   return;
}

// Retrieve the column name.
hr = m_pSearch->GetNextRow(hSearch);

if(FAILED(hr))
{
   return;
}
    
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   wprintf(L"%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```



 

 




