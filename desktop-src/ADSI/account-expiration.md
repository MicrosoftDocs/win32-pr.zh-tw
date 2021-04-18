---
title: '帳戶到期 (LDAP 提供者) '
description: 若要設定帳戶到期日，請將 IADsUser. Iadsuser.accountexpirationdate 屬性設定為所需的日期值。
ms.assetid: d0b90bb3-ad7c-4394-956d-061a915f210d
ms.tgt_platform: multiple
keywords:
- 帳戶到期 ADSI、LDAP 提供者
- LDAP 提供者 ADSI，使用者管理範例，帳戶到期日
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03ea33d8d5abb219c2b562aa05058b5dec45919
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106976341"
---
# <a name="account-expiration-ldap-provider"></a>帳戶到期 (LDAP 提供者) 

若要設定帳戶到期日，請將 [**IADsUser. iadsuser.accountexpirationdate**](iadsuser-property-methods.md) 屬性設定為所需的日期值。 若要停用帳戶到期日，請將 [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) 屬性設定為零。 下列程式碼範例示範如何設定到期日。


```VB
Public Sub SetUserAccountExpirationDate(User As IADsUser, ExpirationDate As Date)
    If 0 = ExpirationDate Then
        ' Disable the account expiration date.
        User.Put "accountExpires", 0
    Else
        ' Set the new account expiration date.
        User.AccountExpirationDate = ExpirationDate
    End If
    
    User.SetInfo
 
End Sub
```




```C++
/***************************************************************************

    SetUserAccountExpirationDate()

***************************************************************************/

HRESULT SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
    if(!pUser) 
    {
        return E_INVALIDARG;
    }

    HRESULT hr;

    if(!date || date < 0) 
    {
        // Account never expires. Set the accountExpires attribute to zero.
        VARIANT var;
        VariantInit(&var);
        V_I4(&var) = 0;
        V_VT(&var) = VT_I4;
        
        hr = pUser->Put(CComBSTR("accountExpires"), var); 

        VariantClear(&var);
    }
    else 
    {
        // Account expires on date.
        hr = pUser->put_AccountExpirationDate(date); 
    }

    if(S_OK == hr)
    {
        hr = pUser->SetInfo();
    }

    return hr;
}
```



> [!Note]  
> [**AccountExpires**](/windows/desktop/ADSchema/a-accountexpires)屬性包含帳戶到期日。 Active Directory 消費者和電腦 MMC 嵌入式管理單元會顯示帳戶結束時的到期日期。 也就是說，Active Directory 消費者和電腦 MMC 嵌入式管理單元會將帳戶到期日顯示為早于 **accountExpires** 屬性所包含日期的一天。

 

 

 