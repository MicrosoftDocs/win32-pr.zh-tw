---
title: '讀取使用者無法變更 (WinNT 提供者的密碼) '
description: 瞭解如何判斷使用者是否有權變更 WinNT 提供者的密碼。 可以授與或拒絕使用者變更密碼的能力。
ms.assetid: b8b8de00-0def-4506-ab73-d03a7e06256d
ms.tgt_platform: multiple
keywords:
- 讀取使用者無法將密碼 (WinNT 提供者) ADSI
- 使用者無法將密碼 (WinNT 提供者) ADSI，讀取
- WinNT 提供者 ADSI、使用者管理範例、使用者無法變更密碼、讀取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761a1ef0a332f1cdfd7dad1b20426b749618ed2286832c7ff16b207cee57c176
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637548"
---
# <a name="reading-user-cannot-change-password-winnt-provider"></a>讀取使用者無法變更 (WinNT 提供者的密碼) 

使用者變更其密碼的能力是可授與或拒絕的許可權。 若要判斷使用者是否已使用 WinNT 提供者授與此許可權，請閱讀 **ADS \_ \_ PASSWD PASSWD \_ 無法 \_ 變更** 使用者物件之 **userFlags** 屬性的旗標。 Ads [**\_ 使用者 \_ 旗標 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)列舉中定義了 **ads 的 \_ UF 密碼無法 \_ \_ \_ 變更** 旗標。

## <a name="example-code"></a>範例程式碼

下列程式碼範例示範如何取得使用者物件之 **userFlags** 屬性的 **ADS \_ \_ PASSWD PASSWD 無法 \_ \_ 變更** 旗標。


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Function UserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String) As Boolean
    UserCannotChangePassword = False
    
    Dim oUser As IADs
    
    strPath = "WinNT://" + strDomain + "/" + strUser
    
    If "" <> strUserCred Then
        Dim dso As IADsOpenDSObject
        
        ' Bind to the group with the specified user name and password.
        Set dso = GetObject("WinNT:")
        Set oUser = dso.OpenDSObject(strPath, strUserCred, strPassword, 1)
    Else
        ' Bind to the group with the current credentials.
        Set oUser = GetObject(strPath)
    End If
    
    If (oUser.Get("userFlags") And ADS_UF_PASSWD_CANT_CHANGE) <> 0 Then
        UserCannotChangePassword = True
    Else
        UserCannotChangePassword = False
    End If
End Function
```



下列程式碼範例示範如何取得使用者物件之 **userFlags** 屬性的 **ADS \_ \_ PASSWD PASSWD 無法 \_ \_ 變更** 旗標。


```C++
//***************************************************************************
//
//  UserCannotChangePassword()
//
//***************************************************************************

HRESULT UserCannotChangePassword(LPCWSTR pwszDomain, 
                                 LPCWSTR pwszUser, 
                                 LPCWSTR pwszUserCred, 
                                 LPCWSTR pwszPassword, 
                                 BOOL *pfCannotChangePassword)
{
    if(NULL == pwszDomain || NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
    *pfCannotChangePassword = FALSE;

    HRESULT hr;
    IADs *pads;

    CComBSTR sbstrADsPath = L"WinNT://";
    sbstrADsPath += pwszDomain;
    sbstrADsPath += "/";
    sbstrADsPath += pwszUser;

    hr = ADsOpenObject( sbstrADsPath,
                        pwszUserCred,
                        pwszPassword,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs, 
                        (void**)&pads);

    if(SUCCEEDED(hr))
    {
        CComVariant svar;
        
        hr = pads->Get(CComBSTR("userFlags"), &svar);
        if(SUCCEEDED(hr))
        {
            if(ADS_UF_PASSWD_CANT_CHANGE & svar.lVal)
            {
                *pfCannotChangePassword = TRUE;
            }
            else
            {
                *pfCannotChangePassword = FALSE;
            }
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




