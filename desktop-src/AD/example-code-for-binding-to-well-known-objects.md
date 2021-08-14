---
title: 系結至已知物件的範例程式碼
description: 本主題包含使用 WKGUID 系結字串系結至已知物件的程式碼範例。
ms.assetid: 59345173-5598-4b0a-976c-c5741b785ce1
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，系結至已知的物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb113e13889dfebdd34adc553ea21693684d6848f9d25bc2bb4c436fe0b71b5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191281"
---
# <a name="example-code-for-binding-to-well-known-objects"></a>系結至已知物件的範例程式碼

下列 c + + 程式碼範例示範如何使用 WKGUID 系結字串來系結至已知的物件。


```C++
//*********************************************************
//
//  BindToWellKnownObject()
//
//  Binds to one of the well-known objects in the current domain 
//  with the current user credentials. pwszGUID must be one of  
//  the GUID strings defined in NTDSAPI.H, such as 
//  GUID_USERS_CONTAINER_W.
//
//******************************************************************

HRESULT BindToWellKnownObject(LPCWSTR pwszGUID, IADs **ppObject)
{
    if(NULL == ppObject)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppObject = NULL;

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

            pwszPath = new WCHAR[lstrlenW(pwszFormat) + 
                           lstrlenW(pwszGUID) + 
                           lstrlenW(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, pwszFormat, pwszGUID, var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADs,
                                (LPVOID*)ppObject);

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



 

 




