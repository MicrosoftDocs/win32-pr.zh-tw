---
title: 取得群組的網域 Account-Style 名稱
description: 使用者、群組、電腦和其他安全性主體可以網域帳戶形式表示。
ms.assetid: 85627d2d-2845-4998-9957-ce0c8b6473bd
ms.tgt_platform: multiple
keywords:
- 群組廣告，取得網域帳戶樣式的群組名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758e61072b862f7c4cd1581b8d54dafb38915be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839319"
---
# <a name="getting-the-domain-account-style-name-of-a-group"></a>取得群組的網域 Account-Style 名稱

使用者、群組、電腦和其他安全性主體可以網域帳戶形式表示。 網域帳戶 (舊版 Windows NT) 所使用的登入名稱格式如下：


```C++
<domain>\<account>
```



其中 " <domain> " 是包含使用者 Windows NT 網域的名稱，而 " <account> " 是指定使用者的 **samAccountName** 屬性。 例如： "Fabrikam \\ jeffsmith"。

網域帳戶表單可以在安全描述項中指定 ACE 內的信任者。 它也會用於執行 Windows 版本 NT 4.0 及更早版本之電腦上的登入名稱。


```C++
// Need to include the following headers to use DsGetDcName.
// #include <LMCONS.H>
// #include <Dsgetdc.h>
// #include <Lmapibuf.h>
// This function returns the previous version name of the security principal 
// specified by the distinguished name specified by szDN.
// The szDomain parameter should be NULL to use the current domain
// to get the name translation. Otherwise, specify the domain to use as the
// domain name (such as liliput) 
// or in dotted format (such as lilliput.Fabrikam.com).
HRESULT GetDownlevelName(LPOLESTR szDomainName, LPOLESTR szDN, LPOLESTR *ppNameString)
{
HRESULT hr = E_FAIL;
IADsNameTranslate *pNameTr = NULL;
IADs *pObject = NULL;
CComBSTR sbstrInitDomain = "";
 
if ((!szDN)||(!ppNameString))
{
    return hr;
}
 
// Use the current domain if none is specified.
if (!szDomainName)
{
    // Call DsGetDcName to get the name of this computer's domain.
    PDOMAIN_CONTROLLER_INFO DomainControllerInfo = NULL;
    DWORD dReturn = 0L;
    dReturn = DsGetDcName(  NULL,
                NULL,
                NULL,
                NULL,
                DS_DIRECTORY_SERVICE_REQUIRED,
                &DomainControllerInfo
    );
    if (dReturn==NO_ERROR)
    {
        sbstrInitDomain = DomainControllerInfo->DomainName;
        hr = S_OK;
    }
 
    // Free the buffer.
    if (DomainControllerInfo)
        NetApiBufferFree(DomainControllerInfo);
}
else
{
    sbstrInitDomain = szDomainName;
    hr = S_OK;
}
 

if (SUCCEEDED(hr))
{
 
    // Create the COM object for the IADsNameTranslate object.
    hr  = CoCreateInstance( 
                                CLSID_NameTranslate,
                                NULL,
                                CLSCTX_INPROC_SERVER,
                                IID_IADsNameTranslate,
                                (void **)&pNameTr
                          );
    if (SUCCEEDED(hr))
    {
 
        // Initialize for the specified domain.
        hr = pNameTr->Init(ADS_NAME_INITTYPE_DOMAIN, sbstrInitDomain);
        if (SUCCEEDED(hr))
        {
            CComBSTR sbstrNameTr;

            hr = pNameTr->Set(ADS_NAME_TYPE_1779, CComBSTR(szDN));
            hr = pNameTr->Get(ADS_NAME_TYPE_NT4, &sbstrNameTr);
            if (SUCCEEDED(hr))
            {
                *ppNameString = (OLECHAR *)CoTaskMemAlloc (sizeof(OLECHAR)*(sbstrNameTr.Length() + 1));
                if (*ppNameString)
                    wcscpy_s(*ppNameString, sbstrNameTr);
                else
                    hr=E_FAIL;
            }
        }

        pNameTr->Release();
    }
}
 
// Caller must call CoTaskMemFree to free ppNameString.
return hr;
}
```



 

 




