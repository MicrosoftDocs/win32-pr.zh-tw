---
title: 使用 >idirectorysearch 介面搜尋
description: '>idirectorysearch 介面提供高階且低額外負荷的介面來查詢目錄或通用類別目錄的資料。'
ms.assetid: da415cb2-f320-4be4-b5bd-053cd6a6b2fd
ms.tgt_platform: multiple
keywords:
- 使用 >idirectorysearch 介面 ADSI 搜尋
- 查詢 ADSI、查詢介面、>idirectorysearch
- ADSI ADSI，範例程式碼 C/c + +，使用 >idirectorysearch 搜尋目錄
- 使用搜尋目錄來 >idirectorysearch ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c46700c48f82955bd01967808cd30f2fa078e3b6c998fb3beaac4bf7c7fe8707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023216"
---
# <a name="searching-with-the-idirectorysearch-interface"></a>使用 >idirectorysearch 介面搜尋

[**>Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面提供高階且低額外負荷的介面來查詢目錄或通用類別目錄的資料。 **>Idirectorysearch** COM 介面只能與 vtable 搭配使用，因此不能用於以 Automation 為基礎的開發環境。

**執行搜尋**

1.  系結至目錄中的物件。
2.  呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 指標。
3.  使用 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 指標執行搜尋。 呼叫 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 方法，並傳遞搜尋篩選、要求的屬性名稱及其他參數。

如需搜尋篩選語法的詳細資訊，請參閱 [搜尋篩選語法](search-filter-syntax.md)。

查詢執行是提供者特定的。 有些提供者在呼叫 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) 或 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 之前，不會執行實際的查詢。 [**>Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面可直接搭配搜尋篩選使用。 SQL 方言和 LDAP 方言都不需要。

[**>Idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面會提供方法來列舉結果集（依資料列）。 [**>Idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)方法會抓取第一個資料列，而 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)會將您移至目前資料列中的下一個資料列。 當您到達最後一個資料列時，呼叫這些方法會傳回 \_ \_ NOMORE 資料 \_ 列錯誤碼的廣告。 相反地， [**>idirectorysearch：： GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) 會一次將您移回一個資料列。 S \_ ADS \_ NOMORE ROWS 傳回 \_ 值指出您已達到結果集的第一個資料列。 這些方法會在用戶端上的結果集（常駐于記憶體中）上運作。 因此，當您執行分頁和非同步搜尋並關閉快取 \_ \_ 結果選項時，回溯滾動可能會產生非預期的結果。

當您找到適當的資料列時，請呼叫 [**>idirectorysearch：： GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn) 來取得資料項目、依資料行的資料行。 每次呼叫時，您都會傳遞感興趣之資料行的名稱。 傳回的資料項目是 [**廣告 \_ 搜尋資料 \_ 行**](/windows/desktop/api/Iads/ns-iads-ads_search_column) 結構的指標。 **GetColumn** 會為您配置此結構，但您必須使用 [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn)來釋放它。 呼叫 [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) 以完成搜尋作業。

**執行目錄搜尋**

1.  系結至 LDAP 提供者。 它可能是網域控制站或通用類別目錄提供者。
2.  使用 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))呼叫來取出 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) COM 介面;這項作業在初始系結期間可能已在步驟1中完成。

    （選擇性）呼叫 [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 來選取用來處理搜尋結果的選項。

3.  呼叫 [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch)。 根據 [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) 中設定的選項而定，這可能會開始執行查詢。
4.  呼叫 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) ，將資料列索引 (內部移至 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)) 至第一個資料列。
5.  使用 [**GetColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getcolumn)讀取資料列中的資料，然後呼叫 [**FreeColumn**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-freecolumn) 釋放 **GetColumn** 所配置的記憶體。
6.  重複步驟5，直到從搜尋結果取出所有資料，或直到 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 傳回 S \_ ADS NOMORE 資料列為止 \_ \_ 。
7.  完成時呼叫 [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) 和 [**CloseSearchHandle**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-closesearchhandle) 。

下列程式碼範例顯示此案例。 若要開始系結至 ADSI，請呼叫 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 函數。


```C++
HRESULT hr = S_OK; // COM result variable
ADS_SEARCH_COLUMN col;  // COL for iterations
LPWSTR szUsername = NULL; // user name
LPWSTR szPassword = NULL; // password
 
// Interface Pointers.
IDirectorySearch     *pDSSearch    =NULL;
 
// Initialize COM.
CoInitialize(0);

// Add code to securely retrieve the user name and password or
// leave both as NULL to use the default security context.
 
// Open a connection with server.
hr = ADsOpenObject(L"LDAP://coho.salmon.Fabrikam.com", 
szUsername,
szPassword,
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



這會提供 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 介面的指標。

現在有一個 IDirectoryInterface 實例的 COM 介面，請呼叫 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)。

建立屬性名稱的陣列，以準備呼叫 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 函數。 屬性名稱是在 Active Directory 的架構內定義。 如需架構定義的詳細資訊，請參閱 [ADSI 架構模型](adsi-schema-model.md)。 如果物件支援，則會傳回所列出的屬性名稱，做為搜尋的結果集。


```C++
LPWSTR pszAttr[] = { L"description", L"Name", L"distinguishedname" };
ADS_SEARCH_HANDLE hSearch;
DWORD dwCount = 0;
DWORD dwAttrNameSize = sizeof(pszAttr)/sizeof(LPWSTR);
```



現在，呼叫 [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) 函數。 除非您呼叫 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 方法，否則搜尋不會執行。


```C++
// Search for all objects with the 'cn' property that start with c.
hr = pDSSearch->ExecuteSearch(L"(cn=c*)",pszAttr ,dwAttrNameSize,&hSearch );
```



呼叫 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 以反覆運算結果中的資料列。 然後，會查詢每個資料列中的 "description" 屬性。 如果找到此屬性，則會顯示該屬性。


```C++
LPWSTR pszColumn;
    while( pDSSearch->GetNextRow( hSearch) != S_ADS_NOMORE_ROWS )
    {
        // Get the property.
        hr = pDSSearch->GetColumn( hSearch, L"description", &col );
 
        // If this object supports this attribute, display it.
        if ( SUCCEEDED(hr) )
        { 
           if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
              wprintf(L"The description property:%s\r\n", col.pADsValues->CaseIgnoreString); 
           pDSSearch->FreeColumn( &col );
        }
        else
            puts("description property NOT available");
        puts("------------------------------------------------");
        dwCount++;
    }
    pDSSearch->CloseSearchHandle(hSearch);
    pDSSearch->Release();
```



若要結束搜尋，請呼叫 [**AbandonSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-abandonsearch) 方法。

請注意，如果未設定頁面大小， [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 會封鎖，直到整個結果集傳回至用戶端為止。 如果已設定頁面大小，則會 **GetNextRow** 封鎖，直到第一個頁面 (頁面大小 = 頁面中的資料列數目) 。 如果已設定頁面大小，而且查詢要排序，且您未搜尋至少一個索引屬性，則會忽略 [頁面大小] 值，而且伺服器會在傳回資料之前計算整個結果集。 這會造成 **GetNextRow** 封鎖，直到查詢完成為止。

> [!Note]  
> 若要將此查詢從目錄搜尋變更為通用類別目錄搜尋， [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) 呼叫會變更。

 


```C++
// Open a connection with the server.
hr = ADsOpenObject(L"GC://coho.salmon.Fabrikam.com", 
szUsername, 
szPassword, 
ADS_SECURE_AUTHENTICATION,
IID_IDirectorySearch,
(void **)&pDSSearch);
```



 

 