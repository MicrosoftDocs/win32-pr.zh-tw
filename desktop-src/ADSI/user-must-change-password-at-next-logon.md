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
ms.openlocfilehash: 784ee0defbe3c8ec9abe2d110c2532b8c9688019
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020782"
---
# <a name="user-must-change-password-at-next-logon-ldap-provider"></a><span data-ttu-id="5741a-107">使用者必須在下次登入時變更密碼 (LDAP 提供者) </span><span class="sxs-lookup"><span data-stu-id="5741a-107">User Must Change Password at Next Logon (LDAP Provider)</span></span>

<span data-ttu-id="5741a-108">若要強制使用者在下次登入時變更其密碼，請將 **pwdLastSet** 屬性設定為零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="5741a-108">To force a user to change their password at next logon, set the **pwdLastSet** attribute to zero (0).</span></span> <span data-ttu-id="5741a-109">若要移除這項需求，請將 **pwdLastSet** 屬性設定為-1。</span><span class="sxs-lookup"><span data-stu-id="5741a-109">To remove this requirement, set the **pwdLastSet** attribute to -1.</span></span> <span data-ttu-id="5741a-110">**PwdLastSet** 屬性不能設定為任何其他值（除了系統以外）。</span><span class="sxs-lookup"><span data-stu-id="5741a-110">The **pwdLastSet** attribute cannot be set to any other value except by the system.</span></span>

<span data-ttu-id="5741a-111">下列程式碼範例顯示如何設定「使用者必須在下次登入時變更密碼」選項。</span><span class="sxs-lookup"><span data-stu-id="5741a-111">The following code example shows how to set the "User must change password at next logon" option.</span></span>


```VB
Dim usr as IADs

Set usr = GetObject("LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=Com")
usr.Put "pwdLastSet", CLng(0)
usr.SetInfo
```



<span data-ttu-id="5741a-112">下列程式碼範例顯示如何設定「使用者必須在下次登入時變更密碼」選項。</span><span class="sxs-lookup"><span data-stu-id="5741a-112">The following code example shows how to set the "User must change password at next logon" option.</span></span>


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



 

 




