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
# <a name="example-code-for-getting-the-distinguished-name-of-the-domain"></a><span data-ttu-id="880d8-104">取得網域辨別名稱的範例程式碼</span><span class="sxs-lookup"><span data-stu-id="880d8-104">Example Code for Getting the Distinguished Name of the Domain</span></span>

<span data-ttu-id="880d8-105">本主題包含的程式碼範例會使用無伺服器系結來取得本機電腦所屬網域的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="880d8-105">This topic includes a code example that gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>

<span data-ttu-id="880d8-106">下列 Visual Basic 程式碼範例會使用無伺服器系結，取得本機電腦所屬網域的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="880d8-106">The following Visual Basic code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```VB
Dim rootDSE As IADs
Dim DistinguishedName As String
 
Set rootDSE = GetObject("LDAP://rootDSE")
DistinguishedName = "LDAP://" & rootDSE.Get("defaultNamingContext")
```



<span data-ttu-id="880d8-107">下列 c # 程式碼範例會使用無伺服器系結，取得本機電腦所屬網域的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="880d8-107">The following C# code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


```CSharp
DirectoryEntry RootDirEntry = new DirectoryEntry("LDAP://RootDSE");
Object distinguishedName = RootDirEntry.Properties["defaultNamingContext"].Value;
```



<span data-ttu-id="880d8-108">下列 C/c + + 程式碼範例會使用無伺服器系結，取得本機電腦所屬網域的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="880d8-108">The following C/C++ code example gets the distinguished name of the domain that the local computer is a member of by using serverless binding.</span></span>


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



 

 




