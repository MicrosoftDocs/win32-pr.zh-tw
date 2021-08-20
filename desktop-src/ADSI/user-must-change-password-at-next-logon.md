---
title: '使用者必須在下次登入時變更密碼 (LDAP 提供者) '
description: 若要強制使用者在下次登入時變更其密碼，請將 pwdLastSet 屬性設定為零 (0) 。 若要移除這項需求，請將 pwdLastSet 屬性設定為-1。 PwdLastSet 屬性不能設定為任何其他值（除了系統以外）。
ms.assetid: 0182151c-ddb7-4d08-98c6-c37e6e514cf0
ms.tgt_platform: multiple
keywords:
- 使用者必須在下次登入 ADSI （LDAP 提供者）時變更密碼
- LDAP 提供者 ADSI、使用者管理範例、使用者必須在下次登入時變更密碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103703381512e82eee608d452b921429c87ef3ce6b7d59017fd07bc081e75ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648838"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a>使用者必須在下次登入時變更密碼 (LDAP 提供者) 

若要強制使用者在下次登入時變更其密碼，請將 **pwdLastSet** 屬性設定為零 (0) 。 若要移除這項需求，請將 **pwdLastSet** 屬性設定為-1。 **PwdLastSet** 屬性不能設定為任何其他值（除了系統以外）。

下列程式碼範例顯示如何設定「使用者必須在下次登入時變更密碼」選項。


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



下列程式碼範例顯示如何設定「使用者必須在下次登入時變更密碼」選項。


```C++
/***************************************************************************

    SetUserMustChangePassword()

***************************************************************************/

HRESULT SetUserMustChangePassword(LPCWSTR pwszUserADsPath, 
                                  LPCWSTR pwszUsername, 
                                  LPCWSTR pwszPassword)
{
    IADs *pUser;
    HRESULT hr;

    hr = ADsOpenObject(pwszUserADsPath,
                        pwszUsername,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&pUser);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        hr = pUser->Put(CComBSTR("pwdLastSet"), var);
        hr = pUser->SetInfo();

        VariantClear(&var);
        pUser->Release();
    }

    return hr;
}
```



 

 




