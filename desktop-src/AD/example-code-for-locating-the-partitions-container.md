---
title: 用於尋找資料分割容器的範例程式碼
description: 本主題包含找出資料分割容器的程式碼範例。
ms.assetid: 7aa6ad5a-7baf-484a-9296-eafb61da5f4e
ms.tgt_platform: multiple
keywords:
- 用於尋找資料分割容器的範例程式碼
- 應用程式目錄分割廣告，用於尋找分割區容器的範例程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3f10156894a71a3308b58d125c16782497e5f29
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "106967469"
---
# <a name="example-code-for-locating-the-partitions-container"></a><span data-ttu-id="85c62-105">用於尋找資料分割容器的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="85c62-105">Example Code for Locating the Partitions Container</span></span>

<span data-ttu-id="85c62-106">本主題包含找出資料分割容器的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="85c62-106">This topic includes code examples that locate the partition container.</span></span>

<span data-ttu-id="85c62-107">下列 C/c + + 程式碼範例會藉由搜尋 [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) 物件的設定容器來取得分割區容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="85c62-107">The following C/C++ code example gets the distinguished name of the Partitions container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span>


```C++
/***************************************************************************

    GetPartitionsDNSearch()

    Description: Gets the distinguished name of the Partitions container in 
    the current enterprise forest.

    Parameters:

    ppwszPartitionsDN - Pointer to an LPWSTR that receives the distinguished 
    name string. The caller must free this memory with 
    FreeADsMem when it is no longer required.

***************************************************************************/

HRESULT GetPartitionsDNSearch(LPWSTR *ppwszPartitionsDN)
{
 
    *ppwszPartitionsDN = NULL;
    
    HRESULT hr;

    IADs *padsRootDSE;

    // Bind to the RootDSE to get the configurationNamingContext property.
    hr = ADsOpenObject( L"LDAP://RootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&padsRootDSE);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;

        // Get the configurationNamingContext property.
        hr = padsRootDSE->Get(CComBSTR("configurationNamingContext"), &svar);
        if(SUCCEEDED(hr))
        {
            IDirectorySearch *pConfigSearch;

            // Bind to the Configuration container.
            CComBSTR sbstrPath = "LDAP://";
            sbstrPath += svar.bstrVal;

            hr = ADsOpenObject( sbstrPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IDirectorySearch, 
                                (LPVOID*)&pConfigSearch);

            if(SUCCEEDED(hr))
            {
                // Search for an object that is of type crossRefContainer.
                ADS_SEARCHPREF_INFO SearchPref[1];

                // Set the search scope.
                SearchPref[0].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
                SearchPref[0].vValue.dwType = ADSTYPE_INTEGER;
                SearchPref[0].vValue.Integer = ADS_SCOPE_ONELEVEL;
                
                hr = pConfigSearch->SetSearchPreference(SearchPref, sizeof(SearchPref)/sizeof(ADS_SEARCHPREF_INFO));
                if(SUCCEEDED(hr))
                {
                    ADS_SEARCH_HANDLE hSearch = NULL;
                    LPWSTR pwszAttributes[1] = {L"distinguishedName"};
                    LPWSTR pwszSearchFilter = L"(&(objectClass=crossRefContainer))";
                    
                    // Execute the search.
                    hr = pConfigSearch->ExecuteSearch(pwszSearchFilter, 
                        pwszAttributes, 
                        sizeof(pwszAttributes)/sizeof(LPWSTR), 
                        &hSearch);
                    if(SUCCEEDED(hr))
                    {
                        // Get the first result row. There should never be more than one match.
                        hr = pConfigSearch->GetFirstRow(hSearch);
                        if(S_OK == hr)
                        {
                            ADS_SEARCH_COLUMN col;

                            // Get the search result. The distinguishedName attribute will be a string.
                            hr = pConfigSearch->GetColumn(hSearch, pwszAttributes[0], &col);
                            if(SUCCEEDED(hr))
                            {
                                // col.pADsValues[0].DNString;
                                DWORD dwChars = lstrlenW(col.pADsValues[0].DNString) + 1;
                                
                                *ppwszPartitionsDN = (LPWSTR)AllocADsMem(dwChars * sizeof(WCHAR));
                                
                                if(*ppwszPartitionsDN)
                                {
                                    wcsncpy_s(*ppwszPartitionsDN, col.pADsValues[0].DNString, dwChars);
                                }
                                else
                                {
                                    hr = E_OUTOFMEMORY;
                                }

                                pConfigSearch->FreeColumn(&col);
                            }
                        }
                        else
                        {
                            hr = HRESULT_FROM_WIN32(ERROR_NOT_FOUND);
                        }
                        
                        // Close the search handle to cleanup.
                        pConfigSearch->CloseSearchHandle(hSearch);
                    }
                }

                pConfigSearch->Release();
            }
        }
        
        padsRootDSE->Release();
    }

    return hr;
}
```



<span data-ttu-id="85c62-108">下列 Visual Basic Scripting Edition 程式碼範例會藉由搜尋 [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) 物件的設定容器來取得分割區容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="85c62-108">The following Visual Basic Scripting Edition code example gets the distinguished name of the Partitions container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span>


```VB
Const ADS_SECURE_AUTHENTICATION = 1

'
'   GetPartitionsDNSearch
'
'   Description: Gets the distinguished name of the Partitions container in
'   the current enterprise forest.
'
Function GetPartitionsDNSearch()
    ' Bind to RootDSE.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    
    Set oConn = CreateObject("ADODB.Connection")
    Set oComm = CreateObject("ADODB.Command")
     
    oConn.Provider = "ADsDSOObject"

    ' Set the binding options for the search.
    oConn.Properties("ADSI Flag") = ADS_SECURE_AUTHENTICATION
    
    oConn.Open
    oComm.ActiveConnection = oConn
    
    oComm.CommandText = "<LDAP://" + oRootDSE.Get("configurationNamingContext") + ">;(&(objectClass=crossRefContainer));distinguishedName;onelevel"
    
    ' WScript.Echo oComm.CommandText
    
    ' Execute the query.
    Set oResults = oComm.Execute
    
    ' Get the first result. This should be the only result.
    Set oField = oResults(0)
    
    GetPartitionsDNSearch = oField.Value
End Function
```



<span data-ttu-id="85c62-109">下列 C/c + + 程式碼範例會手動建立辨別名稱，以取得分割區容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="85c62-109">The following C/C++ code example gets the distinguished name of the Partitions container by manually building the distinguished name.</span></span>


```C++
/***************************************************************************

    GetPartitionsDNManual()

    Description: Gets the distinguished name of the Partitions container in 
    the current enterprise forest.

    Parameters:

    ppwszPartitionsDN - Pointer to an LPWSTR that receives the distinguished 
    name string. The caller must free this memory with 
    FreeADsMem when it is no longer required.

***************************************************************************/

HRESULT GetPartitionsDNManual(LPWSTR *ppwszPartitionsDN)
{

    *ppwszPartitionsDN = NULL;

    HRESULT hr;

    IADs *padsRootDSE;

    // Bind to the RootDSE to get the configurationNamingContext property.
    hr = ADsOpenObject( L"LDAP://RootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (LPVOID*)&padsRootDSE);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;

        // Get the configurationNamingContext property.
        hr = padsRootDSE->Get(CComBSTR("configurationNamingContext"), &svar);
        if(SUCCEEDED(hr))
        {
            CComBSTR sbstrDN = "CN=Partitions,";
            sbstrDN += svar.bstrVal;
            DWORD dwChars = sbstrDN.Length() + 1;

            *ppwszPartitionsDN = (LPWSTR)AllocADsMem(dwChars * sizeof(WCHAR));
            
            if(*ppwszPartitionsDN)
            {
                wcsncpy_s(*ppwszPartitionsDN, sbstrDN.m_str, dwChars);
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }
        }
        
        padsRootDSE->Release();
    }

    return hr;
}
```



<span data-ttu-id="85c62-110">下列 Visual Basic 程式碼範例會藉由手動建立辨別名稱來取得分割區容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="85c62-110">The following Visual Basic code example gets the distinguished name of the Partitions container by manually building the distinguished name.</span></span>


```VB
'
'   GetPartitionsDNManual
'
'   Description: Gets the distinguished name of the Partitions container in
'   the current enterprise forest.
'
Function GetPartitionsDNManual()
    ' Bind to RootDSE.
    Set oRootDSE = GetObject("LDAP://RootDSE")
    
    ' Get the configurationNamingContext property.
    GetPartitionsDNManual = "CN=Partitions," + oRootDSE.Get("configurationNamingContext")
End Function
```



<span data-ttu-id="85c62-111">下列 c # 程式碼範例會藉由搜尋 [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) 物件的設定容器來取得分割區容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="85c62-111">The following C# code example gets the distinguished name of the Partitions container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span> <span data-ttu-id="85c62-112">此範例搭配使用 c # 與 DirectoryServices。</span><span class="sxs-lookup"><span data-stu-id="85c62-112">This example uses C# with System.DirectoryServices.</span></span>


```CSharp
/***************************************************************************

    GetPartitionsDN()

    Description: Gets the distinguished name of the Partition container in 
    the current enterprise forest.

***************************************************************************/

static string GetPartitionsDN()
{
    // Bind to the RootDSE to get the configurationNamingContext property.
    DirectoryEntry RootDSE = new DirectoryEntry("LDAP://RootDSE");
    DirectoryEntry ConfigContainer = new DirectoryEntry("LDAP://" + 
        RootDSE.Properties["configurationNamingContext"].Value);

    // Search for an object that is of type crossRefContainer.
    DirectorySearcher ConfigSearcher = new DirectorySearcher(ConfigContainer);
    ConfigSearcher.Filter = "(&(objectClass=crossRefContainer))";
    ConfigSearcher.PropertiesToLoad.Add("distinguishedName");
    ConfigSearcher.SearchScope = SearchScope.OneLevel;

    SearchResult result = ConfigSearcher.FindOne();

    return result.Properties["distinguishedName"][0].ToString();
}
```



<span data-ttu-id="85c62-113">下列 Visual Basic .NET 程式碼範例會藉由搜尋 [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) 物件的設定容器來取得分割容器的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="85c62-113">The following Visual Basic .NET code example gets the distinguished name of the Partition container by searching the configuration container for the [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) object.</span></span> <span data-ttu-id="85c62-114">此範例使用 Visual Basic .NET 搭配 DirectoryServices。</span><span class="sxs-lookup"><span data-stu-id="85c62-114">This example uses Visual Basic .NET with System.DirectoryServices.</span></span>


```VB
'**************************************************************************
'
'   GetPartitionsDN()
'
'
'   Description: Gets the distinguished name of the Partitions container in 
'   the current enterprise forest.
'
'**************************************************************************

Function GetPartitionsDN() As String
    ' Bind to the RootDSE to get the configurationNamingContext property.
    Dim RootDSE As New DirectoryEntry("LDAP://RootDSE")

    ' Bind to the Configuraiton container.
    Dim Path As String = "LDAP://" + RootDSE.Properties("configurationNamingContext").Value
    Dim ConfigContainer As New DirectoryEntry(Path)

    ' Search for an object that is of type crossRefContainer.
    Dim ConfigSearcher As New DirectorySearcher(ConfigContainer)
    ConfigSearcher.Filter = "(&(objectClass=crossRefContainer))"
    ConfigSearcher.SearchScope = SearchScope.OneLevel

    Dim result As SearchResult = ConfigSearcher.FindOne()

    Return result.Properties("distinguishedName")(0).ToString()
End Function
```



 

 