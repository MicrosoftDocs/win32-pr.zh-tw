---
title: 偵測架構命名衝突的範例程式碼
description: 本主題包含偵測架構命名衝突的程式碼範例。
ms.assetid: e56cefcf-ea34-4217-9aa7-2f0d4a4d06a4
ms.tgt_platform: multiple
keywords:
- 偵測架構命名衝突 AD 的範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 861b7a93a53c47a234b63b5f52887a22557a2d1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671303"
---
# <a name="example-code-for-detecting-schema-naming-collisions"></a><span data-ttu-id="cbbd8-104">偵測架構命名衝突的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="cbbd8-104">Example Code for Detecting Schema Naming Collisions</span></span>

<span data-ttu-id="cbbd8-105">本主題包含偵測架構命名衝突的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="cbbd8-105">This topic includes a code example that detects schema naming collisions.</span></span>

<span data-ttu-id="cbbd8-106">下列 C/c + + 程式碼範例會查詢 **classSchema** 或 **attributeSchema** 物件上索引鍵命名屬性的架構。</span><span class="sxs-lookup"><span data-stu-id="cbbd8-106">The following C/C++ code example queries the schema for the key naming attributes on a **classSchema** or **attributeSchema** object.</span></span>

<span data-ttu-id="cbbd8-107">如果發現衝突的屬性或類別，則會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="cbbd8-107">It returns **TRUE** if conflicting attributes or classes are found.</span></span> <span data-ttu-id="cbbd8-108">如果具有指定之 **cn**、 **lDAPDisplayName**、 **OID**、 **schemaIDGUID** 或 **linkID** 的屬性或類別與架構不衝突，則會傳回 **FALSE** ，因此可以安全地新增至架構。</span><span class="sxs-lookup"><span data-stu-id="cbbd8-108">It returns **FALSE** if the attribute or class with the specified **cn**, **lDAPDisplayName**, **OID**, **schemaIDGUID**, or **linkID** does not conflict with the schema and, therefore, is safe to add to the schema.</span></span>


```C++
/********************************************************************

    FindCollidingAttributesOrClasses()

********************************************************************/

HRESULT FindCollidingAttributesOrClasses(
    IDirectorySearch *pSchemaNC, // IDirectorySearch pointer to 
                                 // schema naming context.
    LPWSTR szName,
    LPWSTR szLDAPDisplayName,
    LPWSTR szOID,
    const GUID * pSchemaIDGUID,
    DWORD dwLinkID, // Value is zero (0) if the attribute is not linked,
                    // or if checking for class.
    BOOL *pfIsColliding)
{
    if (!pSchemaNC || 
        !szName ||
        !szLDAPDisplayName || 
        !szOID || 
        !pSchemaIDGUID)
    {
        return E_POINTER;
    }
 
    HRESULT hr = E_FAIL;
        
    LPWSTR szBuffer = NULL;
        
    hr = ADsEncodeBinaryData((LPBYTE)pSchemaIDGUID, 
                             sizeof(GUID), 
                             &szBuffer);
    if (SUCCEEDED(hr))
    {
        LPWSTR pwszFormatLinkID = L"(|(cn=%s)(lDAPDisplayName=%s)(attributeID=%s)(governsID=%s)(schemaIDGUID=%s)(linkID=%d))";
        LPWSTR pwszFormatNoLinkID = L"(|(cn=%s)(lDAPDisplayName=%s)(attributeID=%s)(governsID=%s)(schemaIDGUID=%s))";
        LPWSTR szFilter = new WCHAR[lstrlenW(pwszFormatLinkID) + 
                                    lstrlenW(szName) + 
                                    lstrlenW(szLDAPDisplayName) + 
                                    lstrlenW(szOID) + 
                                    lstrlenW(szOID) +
                                    lstrlenW(szBuffer) +
                                    20 +
                                    1];

        if(szFilter)
        {
            if (dwLinkID > 0L)
            {
                swprintf_s(szFilter,
                    pwszFormatLinkID,
                    szName,
                    szLDAPDisplayName,
                    szOID,
                    szOID,
                    szBuffer,
                    dwLinkID);
            }
            else
            {
                swprintf_s(szFilter,
                    pwszFormatNoLinkID,
                    szName,
                    szLDAPDisplayName,
                    szOID,
                    szOID,
                    szBuffer);
            }
            
            // Attributes are one-level deep in the Schema 
            // container so only search one level.
            ADS_SEARCHPREF_INFO SearchPrefs[2];
            SearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
            SearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
            SearchPrefs[0].vValue.Integer = ADS_SCOPE_ONELEVEL;

            SearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
            SearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER;
            SearchPrefs[1].vValue.Integer = 1000;
            
            int iCount = 0;
            
            // Set the search preference
            hr = pSchemaNC->SetSearchPreference(
                   SearchPrefs, 
                   sizeof(SearchPrefs)/sizeof(ADS_SEARCHPREF_INFO)
                 );
            if (SUCCEEDED(hr))
            {
                LPWSTR pszAttribs[] = {
                    L"lDAPDisplayName", 
                    L"cn", 
                    L"attributeID", 
                    L"governsID", 
                    L"schemaIDGUID", 
                    L"linkID", 
                    L"objectCategory"
                };

                // Handle used for searching
                ADS_SEARCH_HANDLE hSearch = NULL;
                DWORD x = 0L;
                
                hr = pSchemaNC->ExecuteSearch(szFilter,
                                pszAttribs,
                                sizeof(pszAttribs)/sizeof(LPWSTR),
                                &hSearch);
                if (SUCCEEDED(hr))
                {
                    // Call IDirectorySearch::GetNextRow() 
                    // to retrieve the next row  of data.
                    hr = pSchemaNC->GetFirstRow(hSearch);
                    while (hr != S_ADS_NOMORE_ROWS)
                    {
                        // Keep track of count.
                        iCount++;

                        // Get the next row
                        hr = pSchemaNC->GetNextRow(hSearch);
                    }
            
                    // Close the search handle to cleanup
                    pSchemaNC->CloseSearchHandle(hSearch);

                    if(SUCCEEDED(hr))
                    {
                        if (0 == iCount)
                        {
                            *pfIsColliding = FALSE;
                        }
                        else
                        {
                            *pfIsColliding = TRUE;
                        }

                        hr = S_OK;
                    }
                }
            }

            delete szFilter;
        }
            
        FreeADsMem(szBuffer);
    }
    
    return hr;
}
```



 

 




