---
title: '帳戶已停用 (LDAP 提供者) '
description: 若要停用使用者帳戶，請在 IADsUser 介面中將 AccountDisabled 屬性設定為 TRUE。 這類似于 WinNT 提供者。 下列程式碼範例示範如何停用使用者帳戶。
ms.assetid: 7911baa4-4178-47a9-80eb-11dc608a0ea3
ms.tgt_platform: multiple
keywords:
- 帳戶停用 ADSI、LDAP 提供者
- LDAP 提供者 ADSI，使用者管理範例，帳戶已停用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf753da0770e19504d496be20ba350f79bd4788a797eb5241e68261df844b626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181442"
---
# <a name="account-disabled-ldap-provider"></a>帳戶已停用 (LDAP 提供者) 

若要停用使用者帳戶，請在 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)介面中將 AccountDisabled 屬性設定為 **TRUE** 。 這類似于 WinNT 提供者。 下列程式碼範例示範如何停用使用者帳戶。

## <a name="example-1"></a>範例 1


```VB
Dim usr As IADsUser
On Error GoTo Cleanup

Set usr = GetObject("LDAP:// CN=JeffSmith, OU=Sales, DC=Fabrikam, DC=Com")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If

    Set usr = Nothing
```



## <a name="example-2"></a>範例 2


```C++
IADsUser *pUser = NULL;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"LDAP://serv1/cn=Jeff Smith,cn=Users, dc=Fabrikam, dc=com";
hr = ADsGetObject(adsPath,IID_IADsUser,(void**)&pUser);

if(FAILED(hr)){return;}

hr = pUser->put_AccountDisabled(true);
hr = pUser->SetInfo();
```



 

 




