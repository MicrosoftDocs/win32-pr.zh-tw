---
title: 執行屬性範圍查詢
description: 屬性範圍查詢是搜尋喜好設定，可讓您搜尋要執行的物件辨別名稱值屬性。
ms.assetid: 026fbe17-5df7-4007-9d74-5c0abbe793b1
ms.tgt_platform: multiple
keywords:
- 執行屬性範圍查詢 ADSI
- ADSI、搜尋、>idirectorysearch、其他搜尋選項、屬性範圍查詢
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10f5b666028c5fd46e7394b52a1328370e317bc
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968304"
---
# <a name="performing-an-attribute-scope-query"></a>執行屬性範圍查詢

屬性範圍查詢是搜尋喜好設定，可讓您搜尋要執行的物件辨別名稱值屬性。 要搜尋的屬性可以是單一值或多重值，但必須是 **ADS \_ DN \_ 字串** 類型。 執行搜尋時，ADSI 會列舉屬性的分辨名稱值，然後在辨別名稱所代表的物件上執行搜尋。 例如，如果對群組物件的 [**成員**](/windows/desktop/ADSchema/a-member) 屬性執行屬性範圍搜尋，ADSI 會列舉 **成員** 屬性中的辨別名稱，並搜尋群組的每個成員，以尋找指定的搜尋準則。

如果在非 **ADS \_ DN \_ 字串** 類型的屬性上執行屬性範圍查詢，則搜尋將會失敗。 屬性範圍查詢也需要將 **ads \_ SEARCHPREF \_ 搜尋 \_ 範圍** 喜好設定設為 **ads \_ 範圍 \_ 基底**。 **Ads \_ SEARCHPREF \_ 搜尋 \_ 範圍** 喜好設定會自動設定為 **ADS \_ 範圍 \_ 基底**，但如果 **ads \_ SEARCHPREF \_ 搜尋 \_ 範圍** 喜好設定設定為任何其他值，則 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)將會失敗，並出現 **E \_ ADS \_ 錯誤 \_ 參數**。

屬性範圍查詢的結果可以橫跨多個伺服器，而伺服器可能不會傳回所有傳回的資料列所要求的所有資料。 如果發生這種情況，呼叫 [**>idirectorysearch：： GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 或 [**>idirectorysearch：： GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)抓取最後一個資料列時，ADSI 會 **傳回 \_ ads \_ ERRORSOCCURRED** ，而非 **s \_ ads NOMORE 資料 \_ \_ 列**。

若要指定屬性範圍查詢，請將 **ads \_ SEARCHPREF \_ 屬性 \_ 查詢** 搜尋選項設定為 **ADSTYPE \_ CASE，並忽略將 \_ \_ 字串** 值設定為屬性的 lDAPDisplayName，以搜尋傳遞給 [**>idirectorysearch：： SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)方法的 [**ads \_ SEARCHPREF \_ 資訊**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)陣列。 下列程式碼範例會顯示這項作業。


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
SearchPref.vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
SearchPref.vValue.Boolean = L"member";
```



下列程式碼範例顯示如何使用 **ADS \_ SEARCHPREF \_ 屬性 \_ 查詢** 搜尋選項。


```C++
/***************************************************************************

    SearchGroupMembers()

    Searches the members of a group that are of type user and prints each 
    user's cn and distinguishedName values to the console.

    Parameters:

    pwszGroupDN - Contains the distinguished name of the group whose 
    members will be searched.

***************************************************************************/

HRESULT SearchGroupMembers(LPCWSTR pwszGroupDN)
{
    HRESULT hr;
    CComPtr<IDirectorySearch> spSearch;
    CComBSTR sbstrADsPath;
 
    // Bind to the group and get the IDirectorySearch interface.
    sbstrADsPath = "LDAP://";
    sbstrADsPath += pwszGroupDN;
    hr = ADsOpenObject(sbstrADsPath,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IDirectorySearch,
        (void**)&spSearch);
    if(FAILED(hr))
    {
        return hr;
    }
 
    ADS_SEARCHPREF_INFO SearchPrefs[1];

    // Set the ADS_SEARCHPREF_ATTRIBUTE_QUERY search preference.
    SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBUTE_QUERY;
    SearchPrefs[0].vValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
    SearchPrefs[0].vValue.CaseIgnoreString = L"member";

    // Set the search preferences.
    hr = spSearch->SetSearchPreference(SearchPrefs, sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO));
    if(FAILED(hr))
    {
        return hr;
    }

    ADS_SEARCH_HANDLE hSearch;
    
    // Create the search filter.
    LPWSTR pwszSearchFilter = L"(&(objectClass=user))";
 
    // Set attributes to return.
    LPWSTR rgpwszAttributes[] = {L"cn", L"distinguishedName"};
    DWORD dwNumAttributes = sizeof(rgpwszAttributes)/sizeof(LPWSTR);
 
    // Execute the search.
    hr = spSearch->ExecuteSearch(pwszSearchFilter,
        rgpwszAttributes,
        dwNumAttributes,
        &hSearch);
    if(FAILED(hr))
    {
        return hr;
    }

    // Get the first result row.
    hr = spSearch->GetFirstRow(hSearch);
    while(S_OK == hr)
    {
        ADS_SEARCH_COLUMN col;

        // Enumerate the retrieved attributes.
        for(DWORD i = 0; i < dwNumAttributes; i++)
        {
            hr = spSearch->GetColumn(hSearch, rgpwszAttributes[i], &col);
            if(SUCCEEDED(hr))
            {
                switch(col.dwADsType)
                {
                case ADSTYPE_DN_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].DNString);
                    break;

                case ADSTYPE_CASE_IGNORE_STRING:
                    wprintf(L"%s: %s\n\n", rgpwszAttributes[i], col.pADsValues[0].CaseExactString);
                    break;

                default:
                    break;
                }
                
                // Free the column.
                spSearch->FreeColumn(&col);
            }
        }
        
        // Get the next row.
        hr = spSearch->GetNextRow(hSearch);
    }

    // Close the search handle to cleanup.
    hr = spSearch->CloseSearchHandle(hSearch);

    return hr;
}
```



當執行此搜尋並列舉結果時，它會傳回群組 **成員** 屬性清單中包含的所有使用者物件的 **名稱**、**電話號碼** 和 **office 號碼**。

錯誤處理：屬性範圍查詢的結果可能橫跨多個伺服器，而伺服器可能不會傳回所有傳回的資料列所要求的所有資料。 如果發生這種情況，呼叫 [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) 或 [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow)來抓取最後一個資料列時，ADSI 會傳回 **\_ Ads \_ ERRORSOCCURRED**，而不是 **s \_ ads NOMORE 資料 \_ \_ 列**。

 

 