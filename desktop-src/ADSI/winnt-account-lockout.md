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
ms.openlocfilehash: 0ffeacb18b42beeb20b4af8bf571e611a85ab118
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965668"
---
# <a name="account-lockout-winnt-provider"></a><span data-ttu-id="ab98b-105"> (WinNT 提供者的帳戶鎖定) </span><span class="sxs-lookup"><span data-stu-id="ab98b-105">Account Lockout (WinNT Provider)</span></span>

<span data-ttu-id="ab98b-106">當超過失敗的登入嘗試次數時，使用者帳戶會在 [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) 屬性所指定的分鐘數內遭到鎖定。</span><span class="sxs-lookup"><span data-stu-id="ab98b-106">When the number of failed logon attempts is exceeded, the user account becomes locked out for the number of minutes specified by the [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) attribute.</span></span> <span data-ttu-id="ab98b-107">[**IADsUser. IsAccountLocked**](iadsuser-property-methods.md)屬性看起來就像是用來讀取和修改使用者帳戶鎖定狀態的屬性，但是 WinNT ADSI 提供者有限制使用 **IsAccountLocked** 屬性的限制。</span><span class="sxs-lookup"><span data-stu-id="ab98b-107">The [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) property appears to be the property to use to read and modify the lockout state of a user account, but the WinNT ADSI provider has restrictions that limit the use of the **IsAccountLocked** property.</span></span>

## <a name="resetting-the-account-lockout-status"></a><span data-ttu-id="ab98b-108">重設帳戶鎖定狀態</span><span class="sxs-lookup"><span data-stu-id="ab98b-108">Resetting the Account Lockout Status</span></span>

<span data-ttu-id="ab98b-109">使用 WinNT 提供者時， [**IsAccountLocked**](iadsuser-property-methods.md) 屬性只能設定為 **FALSE**，這會將帳戶解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="ab98b-109">When using the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can only be set to **FALSE**, which unlocks the account.</span></span> <span data-ttu-id="ab98b-110">嘗試將 **IsAccountLocked** 屬性設定為 **TRUE** 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="ab98b-110">Attempting to set the **IsAccountLocked** property to **TRUE** will fail.</span></span> <span data-ttu-id="ab98b-111">只有系統可以鎖定帳戶。</span><span class="sxs-lookup"><span data-stu-id="ab98b-111">Only the system can lock an account.</span></span>

<span data-ttu-id="ab98b-112">下列程式碼範例示範如何使用 Visual Basic 搭配 ADSI 來解除鎖定使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="ab98b-112">The following code example demonstrates how to use Visual Basic with ADSI to unlock a user account.</span></span>


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



<span data-ttu-id="ab98b-113">下列程式碼範例示範如何搭配使用 c + + 和 ADSI 來解除鎖定使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="ab98b-113">The following code example demonstrates how to use C++ with ADSI to unlock a user account.</span></span>


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



## <a name="reading-the-account-lockout-status"></a><span data-ttu-id="ab98b-114">讀取帳戶鎖定狀態</span><span class="sxs-lookup"><span data-stu-id="ab98b-114">Reading the Account Lockout Status</span></span>

<span data-ttu-id="ab98b-115">使用 WinNT 提供者時， [**IsAccountLocked**](iadsuser-property-methods.md) 屬性可以用來判斷帳戶是否遭到鎖定。如果帳戶遭到鎖定， **IsAccountLocked** 屬性將會包含 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ab98b-115">With the WinNT provider, the [**IsAccountLocked**](iadsuser-property-methods.md) property can be used to determine if an account is locked out. If an account is locked out, the **IsAccountLocked** property will contain **TRUE**.</span></span> <span data-ttu-id="ab98b-116">如果未鎖定帳戶， **IsAccountLocked** 屬性將會包含 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ab98b-116">If an account is not locked out, the **IsAccountLocked** property will contain **FALSE**.</span></span>

<span data-ttu-id="ab98b-117">下列程式碼範例示範如何搭配 ADSI 使用 Visual Basic 來判斷帳戶是否已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="ab98b-117">The following code example demonstrates how to use Visual Basic with ADSI to determine if an account is locked out.</span></span>


```VB
Public Function IsAccountLocked(AccountDN As String) As Boolean
    Dim oUser As IADsUser
    
    ' Bind to the object.
    Set oUser = GetObject("WinNT://" + AccountDN)
    
    ' Get the IsAccountLocked property.
    IsAccountLocked = oUser.IsAccountLocked
End Function
```



<span data-ttu-id="ab98b-118">下列程式碼範例示範如何搭配使用 c + + 和 ADSI 來判斷帳戶是否已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="ab98b-118">The following code example demonstrates how to use C++ with ADSI to determine if an account is locked out.</span></span>


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



 

 