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
ms.openlocfilehash: 207fcfd2bd688f5bb6ddcd19dcb9b1a87a2e40ddb0a7db1e63e9457e671f9947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428461"
---
# <a name="example-code-for-searching-for-attributes"></a>用於搜尋屬性的範例程式碼

下列程式碼範例示範如何使用 **ADS \_ SEARCHPREF \_ \_ 僅 ATTRIBTYPES** 搜尋喜好設定，只取出已指派值的屬性名稱。 此範例會初始化 [**ADS \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)結構，並透過呼叫 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面的 [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法來設定搜尋喜好設定。 然後，此範例會呼叫 [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 方法來執行搜尋。


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



 

 




