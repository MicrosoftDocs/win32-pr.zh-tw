---
title: 取得網域辨別名稱的範例程式碼
description: 本主題包含的程式碼範例會使用無伺服器系結來取得本機電腦所屬網域的分辨名稱。
ms.assetid: 2b478c55-4683-48cd-bee9-385eea38d01d
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，取得網域的辨別名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4badd8cd356ce5adfb20470a969e6f7444c010a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183015"
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



 

 




