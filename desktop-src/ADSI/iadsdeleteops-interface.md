---
title: IADsDeleteOps 介面
description: IADsDeleteOps 介面用於基礎目錄存放區的監督和維護常式。 它可以在單一操作中刪除分葉物件和整個子樹。
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- IADsDeleteOps 介面 ADSI
- 使用 IADsDeleteOps ADSI
- ADSI ADSI，範例程式碼 C/c + +，使用 IADsDeleteOps 來刪除整個群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192411e53f54de2a5f73cc043f35cea6787f4b879972b6a69ada4760c175292a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839941"
---
# <a name="iadsdeleteops-interface"></a>IADsDeleteOps 介面

[**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)介面用於基礎目錄存放區的監督和維護常式。 它可以在單一操作中刪除分葉物件和整個子樹。

如果不支援此介面，從 Active Directory 中刪除物件時，將需要以遞迴方式列舉和刪除每個包含的物件。 使用這個介面時，可以使用單一作業來刪除任何容器物件及其所有包含的物件和子物件。

下列程式碼範例會刪除 "Eng" 容器和所有子物件。


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



下列程式碼範例會刪除 "Eng" 容器和所有子物件。


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




