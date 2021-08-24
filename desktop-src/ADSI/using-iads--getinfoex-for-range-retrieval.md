---
title: 使用 IADs GetInfoEx 進行範圍抓取
description: IADs. GetInfoEx 方法可以用來取得屬性值的範圍。 要取出的值範圍是在傳遞給方法的屬性名稱陣列中指定。
ms.assetid: 2098862f-e5ec-4912-a941-8faceade22ee
ms.tgt_platform: multiple
keywords:
- 使用 IADs GetInfoEx 進行範圍抓取 ADSI
- IADs GetInfoEx ADSI，使用進行範圍抓取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218f6cf8c0b0346a5b5554f870f5729bd55f8b221a3ebe0e425305333ee00cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082192"
---
# <a name="using-iadsgetinfoex-for-range-retrieval"></a>使用 IADs：： GetInfoEx 進行範圍抓取

[**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)方法可以用來取得屬性值的範圍。 要取出的值範圍是在傳遞給方法的屬性名稱陣列中指定。

屬性查詢的範圍規範需要下列格式：


```C++
<property name>;range=<low range>-<high range>
```



其中「 &lt; 屬性名稱」 &gt; 是屬性（attribute）的 **ldapDisplayName** ，「 &lt; 低範圍」 &gt; 是要抓取之第一個屬性值的以零為起始的索引，而「 &lt; 高範圍」 &gt; 是要抓取之最後一個屬性值的以零為起始的索引。 「範圍下限」會使用零 &lt; &gt; 來指定第一個專案。 萬用字元 (\*) 可用於「 &lt; 高範圍」 &gt; 以指定所有剩餘的專案。

下列程式碼範例包含的函式會示範如何搭配 [**IADs：： GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) 使用範圍抓取來列舉群組的成員。


```C++
HRESULT EnumGroupWithGetInfoEx(LPCWSTR pwszGroupDN, 
                               LPCWSTR pwszUsername, 
                               LPCWSTR pwszPassword)
{
    if(NULL == pwszGroupDN)
    {
        return E_POINTER;
    }
    
    HRESULT hr;
    IADs *pads;

    hr = ADsOpenObject( pwszGroupDN,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        const DWORD dwStep = 1000;
        DWORD dwLowRange;
        DWORD dwHighRange;
        WCHAR wszAttr[MAX_PATH];
        LPWSTR rgAttrs[1];

        rgAttrs[0] = wszAttr;

        dwLowRange = 0;
        dwHighRange = dwLowRange + (dwStep - 1);

        do
        {
            VARIANT var;

            // Perform this query with the "range=<lowRange>-<highRange>" range.
            swprintf_s(wszAttr, L"member;range=%d-%d", dwLowRange, dwHighRange);
    
            hr = ADsBuildVarArrayStr(rgAttrs, 1, &var);
            if(SUCCEEDED(hr))
            {
                hr = pads->GetInfoEx(var, 0);
                
                VariantClear(&var);

                if(SUCCEEDED(hr))
                {
                    hr = pads->Get(CComBSTR("member"), &var);
                    if(SUCCEEDED(hr))
                    {
                        if(var.vt == (VT_VARIANT | VT_ARRAY))
                        {
                            VARIANT *pVar;
                            long lLBound, lUBound;

                            // Get the array of VARIANTs.
                            hr = SafeArrayAccessData((SAFEARRAY*)(var.pparray), (void HUGEP* FAR*)&pVar);
                            if(SUCCEEDED(hr))
                            {
                                // Get the bounds for the array.
                                hr = SafeArrayGetLBound((SAFEARRAY*)(var.pparray), 1, &lLBound);
                                hr = SafeArrayGetUBound((SAFEARRAY*)(var.pparray), 1, &lUBound);

                                // Get the number of elements.
                                long cElements = lUBound - lLBound + 1;

                                // Enumerate the elements.
                                for(long i = 0; i < cElements; i++)
                                {
                                    switch(pVar[i].vt)
                                    {
                                    case VT_BSTR:
                                        wprintf(pVar[i].bstrVal); 
                                        wprintf(L"\n"); 
                                        break;
                                    }
                                }

                                // Release the array.
                                SafeArrayUnaccessData((SAFEARRAY*)(var.pparray));
                            }
                        }
                        // This occurs only if one element is retrieved.
                        else if (var.vt == VT_BSTR)
                        {
                            wprintf(var.bstrVal); 
                            wprintf(L"\n"); 
                        }

                        VariantClear(&var);
                    }

                    // Increment the high and low ranges to query for the next block of objects.
                    dwLowRange = dwHighRange + 1;
                    dwHighRange = dwLowRange + (dwStep - 1);
                }
            }
        }while(SUCCEEDED(hr));

        pads->Release();
    }

    return hr;
}
```



下列程式碼範例包含一個函式，該函式會示範如何使用 [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) 的範圍抓取來列舉群組的成員。


```VB
Private Sub EnumGroupMembersWithGetInfoEx(strGroupDN As String, strUsername As String, strPassword As String)
    Dim oGroup As IADs
    Dim dso As IADsOpenDSObject
    
    On Error GoTo quit
        
    strPath = "LDAP://" & strGroupDN
    
    If "" <> strUsername Then
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("LDAP:")
        Set oGroup = dso.OpenDSObject(strPath, strUsername, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oGroup = GetObject(strPath)
    End If
    
    ' For compatibility with all operating systems, the number of objects
    ' retrieved by each query should not exceed 999. The number of objects
    ' to retrieve should be as close as possible to 999 to reduce the number
    ' of round trips to the server necessary to retrieve the objects.
    rangeStep = 999
    lowRange = 0
    highRange = lowRange + rangeStep
    
    Do
        ' Use the "member;range=<lowRange>-<highRange>" syntax.
        strCommandText = "member;range=" & lowRange & "-" & highRange
        Debug.Print "Current search command: " & strCommandText
        
        ' Load the specified range of members into the local cache. This will
        ' throw an error if the range exceeds the properties contained in the
        ' object. The "On Error GoTo quit" error handler will cause the loop
        ' to terminate when this happens.
        On Error GoTo quit
        oGroup.GetInfoEx Array(strCommandText), 0
        
        ' Enumerate the retrieved members.
        oMembers = oGroup.Get("member")
        If vbArray And VarType(oMembers) Then
            For Each oMember In oMembers
                ' Add the member.
                Debug.Print oMember
                nRetrieved = nRetrieved + 1
            Next
        Else
            ' oGroup.Get returned only one member, so add it to the list.
            Debug.Print oMembers
            nRetrieved = nRetrieved + 1
        End If
        
        ' Increment the high and low ranges to query for the next block of objects.
        lowRange = highRange + 1
        highRange = lowRange + rangeStep
    Loop While True
    
quit:
End Sub
```



 

 




