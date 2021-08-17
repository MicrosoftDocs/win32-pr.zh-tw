---
title: " (WinNT 提供者的帳戶鎖定) "
description: 當超過失敗的登入嘗試次數時，使用者帳戶會在 lockoutDuration 屬性所指定的分鐘數內遭到鎖定。
ms.assetid: d7c4134a-0712-4809-83ec-cc09e87afae9
ms.tgt_platform: multiple
keywords:
- 帳戶鎖定 ADSI，WinNT 提供者
- WinNT 提供者 ADSI、使用者管理範例、帳戶鎖定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e28c2a4bf58f5559070af78ca55235e8b10c16b2b856a63a256767d4d67a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838358"
---
# <a name="account-lockout-winnt-provider"></a> (WinNT 提供者的帳戶鎖定) 

當超過失敗的登入嘗試次數時，使用者帳戶會在 [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) 屬性所指定的分鐘數內遭到鎖定。 [**IADsUser. IsAccountLocked**](iadsuser-property-methods.md)屬性看起來就像是用來讀取和修改使用者帳戶鎖定狀態的屬性，但是 WinNT ADSI 提供者有限制使用 **IsAccountLocked** 屬性的限制。

## <a name="resetting-the-account-lockout-status"></a>重設帳戶鎖定狀態

使用 WinNT 提供者時， [**IsAccountLocked**](iadsuser-property-methods.md) 屬性只能設定為 **FALSE**，這會將帳戶解除鎖定。 嘗試將 **IsAccountLocked** 屬性設定為 **TRUE** 將會失敗。 只有系統可以鎖定帳戶。

下列程式碼範例示範如何使用 Visual Basic 搭配 ADSI 來解除鎖定使用者帳戶。


```VB
Public Sub UnlockAccount(AccountDN As String)
    Dim usr As IADsUser
    
    ' Bind to the user account.
    Set usr = GetObject("WinNT://" + AccountDN)
    
    ' Set the IsAccountLocked property to False
    usr.IsAccountLocked = False
    
    ' Flush the cached attributes to the server.
    usr.SetInfo
End Sub
```



下列程式碼範例示範如何搭配使用 c + + 和 ADSI 來解除鎖定使用者帳戶。


```C++
HRESULT UnlockAccount(LPCWSTR pwszUserDN)
{
    if(!pwszUserDN)
    {
        return E_INVALIDARG;
    }

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    // Set the IsAccountLocked property to FALSE;
    hr = spADsUser->put_IsAccountLocked(VARIANT_FALSE);

    // Commit the changes to the server.
    hr = spADsUser->SetInfo();

    return hr;
}
```



## <a name="reading-the-account-lockout-status"></a>讀取帳戶鎖定狀態

使用 WinNT 提供者時， [**IsAccountLocked**](iadsuser-property-methods.md) 屬性可以用來判斷帳戶是否遭到鎖定。如果帳戶遭到鎖定， **IsAccountLocked** 屬性將會包含 **TRUE**。 如果未鎖定帳戶， **IsAccountLocked** 屬性將會包含 **FALSE**。

下列程式碼範例示範如何搭配 ADSI 使用 Visual Basic 來判斷帳戶是否已被鎖定。


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



下列程式碼範例示範如何搭配使用 c + + 和 ADSI 來判斷帳戶是否已被鎖定。


```C++
HRESULT IsAccountLocked(LPCWSTR pwszUserDN, BOOL *pfLocked)
{
    if(!pwszUserDN || !pfLocked)
    {
        return E_INVALIDARG;
    }

    *pfLocked = FALSE;

    // Build the ADsPath.
    CComBSTR sbstr = "WinNT://";
    sbstr += pwszUserDN;
    
    HRESULT hr;
    CComPtr<IADsUser> spADsUser;

    // Bind to the object.
    hr = ADsOpenObject(sbstr,
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION,
        IID_IADsUser,
        (void**)&spADsUser);
    if(S_OK != hr)
    {
        return hr;
    }
    
    VARIANT_BOOL vfLocked;
    hr = spADsUser>get_IsAccountLocked(&vfLocked);
    if(S_OK != hr)
    {
        return hr;
    }

    *pfLocked = (vfLocked != 0);

    return hr;
}
```



 

 