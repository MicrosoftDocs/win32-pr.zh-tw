---
title: 正在抓取刪除的物件
description: 刪除的物件會儲存在刪除的物件容器中。
ms.assetid: dc9a6466-204b-4a78-b0f3-9c03c13a374b
ms.tgt_platform: multiple
keywords:
- 正在抓取刪除的物件 AD
- 物件廣告，正在抓取刪除的物件
- Active Directory，使用來抓取已刪除的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b033a992599fecfc372bf578c1bade54867fd8332c3e114103a69264f736b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025086"
---
# <a name="retrieving-deleted-objects"></a>正在抓取刪除的物件

刪除的物件會儲存在刪除的物件容器中。 「刪除的物件」容器通常不可見，但是「刪除的物件」容器可由「系統管理員」群組的成員來系結。 您可以列舉已刪除物件容器的內容，而且可以使用 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 介面與 **ADS \_ SEARCHPREF \_** 標記搜尋喜好設定，來取得個別已刪除的物件屬性。

您可以藉由系結至 Ntdsapi 中定義的已知 GUID **guid \_ Deleted \_ Objects \_ 容器** 來取得已刪除的物件容器。 如需有關系結至已知 Guid 的詳細資訊，請參閱 [使用 WKGUID 系結至 Well-Known 物件](binding-to-well-known-objects-using-wkguid.md)。

系結至已刪除的物件容器時，指定 **ADS \_ FAST \_** 系結選項。 這表示，用來處理 Active Directory Domain Services 中的物件（例如 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADSPROPERTYLIST**](/windows/desktop/api/iads/nn-iads-iadspropertylist)）的 ADSI 介面，不能用於已刪除的物件容器。 如需詳細資訊和示範如何系結至 Deleted Objects 容器的程式碼範例，請參閱下面的 GetDeletedObjectsContainer 範例函式。

-   [列舉已刪除的物件](#enumerating-deleted-objects)
-   [尋找特定已刪除的物件](#finding-a-specific-deleted-object)
    -   [GetDeletedObjectsContainer](#getdeletedobjectscontainer)
    -   [EnumDeletedObjects](#enumdeletedobjects)
    -   [FindDeletedObjectByGUID](#finddeletedobjectbyguid)

## <a name="enumerating-deleted-objects"></a>列舉已刪除的物件

[**>Idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch)介面是用來搜尋已刪除的物件。

**列舉已刪除的物件**

1.  取得已刪除物件容器的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 介面。 這是藉由系結至已刪除的物件容器來完成，並要求 **>idirectorysearch** 介面。 如需詳細資訊和示範如何系結至 Deleted Objects 容器的程式碼範例，請參閱下列 **GetDeletedObjectsContainer** 函數範例。
2.  使用 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference)方法，將 **ads \_ SEARCHPREF \_ 搜尋 \_ 範圍** 搜尋喜好設定設為 **ads \_ 範圍 \_ ONELEVEL** 。 您也可以使用 **ads \_ 範圍 \_ 子樹** 喜好設定，但刪除的物件容器只是一個層級，因此使用 **ADS \_ 範圍 \_ 子樹** 是多餘的。
3.  將 **ADS \_ SEARCHPREF \_** 標記搜尋喜好設定設定為 **TRUE**。 這會導致搜尋包含已刪除的物件。
4.  將 **ADS \_ SEARCHPREF \_ PAGESIZE** 搜尋喜好設定設定為小於或等於1000的值。 這是選擇性的，但如果沒有這麼做，就無法抓取超過1000的已刪除物件。
5.  將 [**>idirectorysearch：： ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) 呼叫中的搜尋篩選設定為 " (IsDeleted =**TRUE**) "。 這會導致搜尋只取出 **isDeleted** 屬性設定為 **TRUE** 的物件。

如需示範如何列舉已刪除之物件的程式碼範例程式碼，請參閱下列 **EnumDeletedObjects** 函數範例。

您可以新增至搜尋篩選，以進一步調整搜尋，如 [LDAP 方言](/windows/desktop/ADSI/ldap-dialect)所示。 例如，若要搜尋名稱開頭為 "Jeff" 的所有已刪除物件，搜尋篩選準則會設定為 " (& (isDeleted =**TRUE**)  (Cn = Jeff \*) ) "。

因為刪除的物件在刪除時已移除大部分的屬性，所以無法直接系結至已刪除的物件。 系結至已刪除的物件時，必須指定 **ADS \_ FAST \_ BIND** 選項。 這表示，用來處理 Active Directory Domain Services 物件（例如 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 和 [**IADSPROPERTYLIST**](/windows/desktop/api/iads/nn-iads-iadspropertylist)）的 ADSI 介面不能用於已刪除的物件容器。

## <a name="finding-a-specific-deleted-object"></a>尋找特定已刪除的物件

您也可以找到特定已刪除的物件。 如果已知物件的 **objectGUID** ，它可以用來搜尋具有該特定 **objectGUID** 的物件。 如需詳細資訊和示範如何尋找特定已刪除物件的程式碼範例，請參閱下面的 **FindDeletedObjectByGUID** 。

### <a name="getdeletedobjectscontainer"></a>GetDeletedObjectsContainer

下列 c + + 程式碼範例示範如何系結至已刪除的物件容器。


```C++
//***************************************************************************
//
//  GetDeletedObjectsContainer()
//
//  Binds to the Deleted Object container.
//
//***************************************************************************

HRESULT GetDeletedObjectsContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + wcslen(GUID_DELETED_OBJECTS_CONTAINER_W) + wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, GUID_DELETED_OBJECTS_CONTAINER_W, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_FAST_BIND | ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}

```



### <a name="enumdeletedobjects"></a>EnumDeletedObjects

下列 c + + 程式碼範例顯示如何列舉 Deleted Objects 容器中的物件。


```C++
//***************************************************************************
//
//  EnumDeletedObjects()
//
//  Enumerates all of the objects in the Deleted Objects container.
//
//***************************************************************************

HRESULT EnumDeletedObjects()
{
    HRESULT hr;
    IADsContainer *pDeletedObjectsCont = NULL;
    IDirectorySearch *pSearch = NULL;

    hr = GetDeletedObjectsContainer(&pDeletedObjectsCont);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    hr = pDeletedObjectsCont->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Only search for direct child objects of the container.
    ADS_SEARCHPREF_INFO rgSearchPrefs[3];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the page size.
    rgSearchPrefs[2].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
    rgSearchPrefs[2].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[2].vValue.Integer = 1000;

    // Set the search preference
    hr = pSearch->SetSearchPreference(rgSearchPrefs, ARRAYSIZE(rgSearchPrefs));
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    LPWSTR pszSearch = L"(cn=*)";

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search
    hr = pSearch->ExecuteSearch(    pszSearch,
                                    rgAttributes,
                                    ARRAYSIZE(rgAttributes),
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;
                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pDeletedObjectsCont)
    {
        pDeletedObjectsCont->Release();
    }

    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}

```



### <a name="finddeletedobjectbyguid"></a>FindDeletedObjectByGUID

下列 c + + 程式碼範例示範如何從物件的 **objectGUID** 屬性尋找特定已刪除的物件。


```C++
HRESULT FindDeletedObjectByGUID(IADs *padsDomain, GUID *pguid)
{
    HRESULT hr;
    IDirectorySearch *pSearch = NULL;
    LPWSTR pwszGuid = NULL;

    hr = padsDomain->QueryInterface(IID_IDirectorySearch, (LPVOID*)&pSearch);    
    if(FAILED(hr))
    {
        goto cleanup;
    }

    ADS_SEARCH_HANDLE hSearch;

    // Search the entire tree.
    ADS_SEARCHPREF_INFO rgSearchPrefs[2];
    rgSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
    rgSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
    rgSearchPrefs[0].vValue.Integer = ADS_SCOPE_SUBTREE;

    // Search for deleted objects.
    rgSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_TOMBSTONE;
    rgSearchPrefs[1].vValue.dwType = ADSTYPE_BOOLEAN;
    rgSearchPrefs[1].vValue.Boolean = TRUE;

    // Set the search preference.
    hr = pSearch->SetSearchPreference(rgSearchPrefs, 2);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    // Set the search filter.
    hr = ADsEncodeBinaryData((LPBYTE)pguid, sizeof(GUID), &pwszGuid);
    if(FAILED(hr))
    {
        goto cleanup;
    }

    LPWSTR pwszFormat = L"(objectGUID=%s)";

    LPWSTR pwszSearch = new WCHAR[lstrlenW(pwszFormat) + lstrlenW(pwszGuid) + 1];
    if(NULL == pwszSearch)
    {
        goto cleanup;
    }
    
    swprintf_s(pwszSearch, pwszFormat, pwszGuid);
    
    FreeADsMem(pwszGuid);

    // Set the attributes to retrieve.
    LPWSTR rgAttributes[] = {L"cn", L"distinguishedName", L"lastKnownParent"};

    // Execute the search.
    hr = pSearch->ExecuteSearch(    pwszSearch,
                                    rgAttributes,
                                    3,
                                    &hSearch);
    if(SUCCEEDED(hr))
    {    
        // Call IDirectorySearch::GetNextRow() to retrieve the next row of data.
        while(S_OK == (hr = pSearch->GetNextRow(hSearch)))
        {
            ADS_SEARCH_COLUMN col;
            UINT i;
            
            // Enumerate the retrieved attributes.
            for(i = 0; i < ARRAYSIZE(rgAttributes); i++)
            {
                hr = pSearch->GetColumn(hSearch, rgAttributes[i], &col);
                if(SUCCEEDED(hr))
                {
                    switch(col.dwADsType)
                    {
                        case ADSTYPE_CASE_IGNORE_STRING:
                        case ADSTYPE_DN_STRING:
                        case ADSTYPE_PRINTABLE_STRING:
                        case ADSTYPE_NUMERIC_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                wprintf(col.pADsValues[x].CaseIgnoreString); 
                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                        case ADSTYPE_OCTET_STRING:
                            wprintf(L"%s: ", rgAttributes[i]); 
                            for(DWORD x = 0; x < col.dwNumValues; x++)
                            {
                                GUID guid;
                                LPBYTE pb = col.pADsValues[x].OctetString.lpValue;
                                WCHAR wszGUID[MAX_PATH];

                                // Convert the octet string into a GUID.
                                guid.Data1 = *((long*)pb);
                                pb += sizeof(guid.Data1);
                                guid.Data2 = *((short*)pb);
                                pb += sizeof(guid.Data2);
                                guid.Data3 = *((short*)pb);
                                pb += sizeof(guid.Data3);
                                CopyMemory(&guid.Data4, pb, sizeof(guid.Data4));

                                // Convert the GUID into a string.
                                StringFromGUID2(guid, wszGUID, MAX_PATH);
                                wprintf(wszGUID);

                                if((x + 1) < col.dwNumValues)
                                {
                                    wprintf(L","); 
                                }
                                OutputDebugStringW(wszGUID);
                                OutputDebugStringW(L"\n");

                                {
                                    DWORD a;

                                    for(a = 0, *wszGUID = 0; a < col.pADsValues[x].OctetString.dwLength; a++)
                                    {
                                        swprintf_s(wszGUID + lstrlenW(wszGUID), L"%02X", *(LPBYTE)(col.pADsValues[x].OctetString.lpValue + a));
                                    }

                                    OutputDebugStringW(wszGUID);
                                    OutputDebugStringW(L"\n");
                                }
                            }
                            wprintf(L"\n"); 
                            break;

                    }

                    pSearch->FreeColumn(&col);
                }
            }

            wprintf(L"\n");
        }

        // Close the search handle to cleanup.
        pSearch->CloseSearchHandle(hSearch);
    }

cleanup:

    if(pwszSearch)
    {
        delete pwszSearch;
    }
    
    if(pSearch)
    {
        pSearch->Release();
    }

    return hr;
}
```



 

 