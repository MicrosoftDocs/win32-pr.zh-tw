---
title: 取得網域辨別名稱的範例程式碼
description: 本主題包含的程式碼範例會使用無伺服器系結來取得本機電腦所屬網域的分辨名稱。
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，取得網域的辨別名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ebf027e6c95915e34b70f942fdbf342b3f49b9695d7885c442f015d2a74077
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693642"
---
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a>取得網域辨別名稱的範例程式碼

本主題包含的程式碼範例會使用無伺服器系結來取得本機電腦所屬網域的分辨名稱。

下列 Visual Basic 程式碼範例會使用無伺服器系結，取得本機電腦所屬網域的分辨名稱。


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



下列 c # 程式碼範例會使用無伺服器系結，取得本機電腦所屬網域的分辨名稱。


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



下列 C/c + + 程式碼範例會使用無伺服器系結，取得本機電腦所屬網域的分辨名稱。


```C++
IADs *pads;
hr = ADsGetObject(  L"LDAP://rootDSE",
                    IID_IADs, 
                    (void**)&pads);

if(SUCCEEDED(hr))
{
    VARIANT var;

    VariantInit(&var);
    
    hr = pads->Get(CComBSTR("defaultNamingContext"), &var);
    if(SUCCEEDED(hr))
    {
        if(VT_BSTR == var.vt)
        {
            wprintf(var.bstrVal);
        }
        
        VariantClear(&var);
    }
    
    pads->Release();
}
```



 

 




