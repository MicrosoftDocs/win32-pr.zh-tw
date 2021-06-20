---
title: '修改使用者無法變更 (WinNT 提供者的密碼) '
description: 瞭解如何拒絕使用者變更 WinNT 提供者密碼的許可權。 可授與或拒絕使用者變更其密碼的能力。
ms.assetid: 071a817b-087e-49ee-af1a-6f190493cac0
ms.tgt_platform: multiple
keywords:
- '修改使用者無法變更 (WinNT 提供者的密碼) '
- 使用者無法將密碼 (WinNT 提供者) ，修改
- WinNT 提供者 ADSI、使用者管理範例、使用者無法變更密碼、修改
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33510fa36285fa49a413b84d91e29f8d5a367622
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408091"
---
# <a name="modifying-user-cannot-change-password-winnt-provider"></a><span data-ttu-id="c2a8b-107">修改使用者無法變更 (WinNT 提供者的密碼) </span><span class="sxs-lookup"><span data-stu-id="c2a8b-107">Modifying User Cannot Change Password (WinNT Provider)</span></span>

<span data-ttu-id="c2a8b-108">使用者變更其密碼的能力是可授與或拒絕的許可權。</span><span class="sxs-lookup"><span data-stu-id="c2a8b-108">The ability of a user to change their own password is a permission that can be granted or denied.</span></span> <span data-ttu-id="c2a8b-109">若要拒絕此許可權，請將 ADS 的 [無法 **\_ \_ \_ \_ 變更** ] 旗標新增至使用者物件的 **userFlags** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c2a8b-109">To deny this permission, add the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag to the **userFlags** property of the user object.</span></span> <span data-ttu-id="c2a8b-110">若要授與此許可權，請從使用者物件的 **userFlags** 屬性中移除 ADS 的 [ **\_ UF \_ 密碼無法 \_ \_ 變更**] 旗標。</span><span class="sxs-lookup"><span data-stu-id="c2a8b-110">To grant this permission, remove the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag from the **userFlags** property of the user object.</span></span>

## <a name="example-code"></a><span data-ttu-id="c2a8b-111">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="c2a8b-111">Example Code</span></span>

<span data-ttu-id="c2a8b-112">下列程式碼範例示範如何變更使用者物件之 **userFlags** 屬性的 **ADS \_ \_ PASSWD PASSWD 無法 \_ \_ 變更** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c2a8b-112">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```VB
Const ADS_UF_PASSWD_CANT_CHANGE = &H40

Sub SetUserCannotChangePassword(strDomain As String, strUser As String, strUserCred As String, strPassword As String, fUserCannotChangePassword As Boolean)
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
    
    lUserFlags = oUser.Get("userFlags")
    
    If fUserCannotChangePassword Then
        lUserFlags = lUserFlags Or ADS_UF_PASSWD_CANT_CHANGE
    Else
        lUserFlags = lUserFlags And Not ADS_UF_PASSWD_CANT_CHANGE
    End If
    
    ' Modify the userFlags property.
    oUser.Put "userFlags", lUserFlags
    
    ' Commit the changes to the server.
    oUser.SetInfo
End Sub
```



<span data-ttu-id="c2a8b-113">下列程式碼範例示範如何變更使用者物件之 **userFlags** 屬性的 **ADS \_ \_ PASSWD PASSWD 無法 \_ \_ 變更** 旗標。</span><span class="sxs-lookup"><span data-stu-id="c2a8b-113">The following code example shows how to change the **ADS\_UF\_PASSWD\_CANT\_CHANGE** flag of the **userFlags** property of a user object.</span></span>


```C++
//***************************************************************************
//  SetUserCannotChangePassword()
//***************************************************************************

HRESULT SetUserCannotChangePassword(LPCWSTR pwszDomain,
                                    LPCWSTR pwszUser, 
                                    LPCWSTR pwszUserCred, 
                                    LPCWSTR pwszPassword,
                                    BOOL fCannotChangePassword)
{
    if(NULL == pwszDomain || 
        NULL == pwszUser)
    {
        return E_INVALIDARG;
    }
    
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
        CComBSTR sbstrPropName = "userFlags";
        CComVariant svar;
        
        hr = pads->Get(sbstrPropName, &svar);
        if(SUCCEEDED(hr))
        {
            if(fCannotChangePassword)
            {
                svar.lVal |= ADS_UF_PASSWD_CANT_CHANGE;
            }
            else
            {
                svar.lVal &= ~ADS_UF_PASSWD_CANT_CHANGE;
            }

            // Perform the change.
            hr = pads->Put(sbstrPropName, svar);

            // Commit the change.
            hr = pads->SetInfo();
        }
        
        pads->Release();
    }

    return hr;
}
```



 

 




