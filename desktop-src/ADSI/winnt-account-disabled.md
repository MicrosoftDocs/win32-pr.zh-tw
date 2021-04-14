---
title: '帳戶已停用 (WinNT 提供者) '
description: 使用 WinNT 提供者時，可以使用 IADsUser AccountDisabled 屬性來啟用或停用帳戶。
ms.assetid: a3d855cc-5e3d-49c2-b61e-3b35064002ea
ms.tgt_platform: multiple
keywords:
- '帳戶已停用 (WinNT 提供者) '
- 帳戶停用 ADSI，WinNT 提供者
- WinNT 提供者 ADSI，使用者管理範例，帳戶已停用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a99b1fe45b71eda14547703f8721b2a13d581b8e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104386412"
---
# <a name="account-disabled-winnt-provider"></a><span data-ttu-id="7ab7a-106">帳戶已停用 (WinNT 提供者) </span><span class="sxs-lookup"><span data-stu-id="7ab7a-106">Account Disabled (WinNT Provider)</span></span>

<span data-ttu-id="7ab7a-107">使用 WinNT 提供者時，可以使用 [**IADsUser AccountDisabled**](iadsuser-property-methods.md) 屬性來啟用或停用帳戶。</span><span class="sxs-lookup"><span data-stu-id="7ab7a-107">When using the WinNT provider, an account can be enabled or disabled using the [**IADsUser.AccountDisabled**](iadsuser-property-methods.md) property.</span></span>

## <a name="example-1"></a><span data-ttu-id="7ab7a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7ab7a-108">Example 1</span></span>

<span data-ttu-id="7ab7a-109">下列程式碼範例示範如何使用 Visual Basic 搭配 ADSI 來停用帳戶。</span><span class="sxs-lookup"><span data-stu-id="7ab7a-109">The following code example shows how to disable an account using Visual Basic with ADSI.</span></span>


```VB
Dim usr as IADsUser
On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountDisabled = TRUE ' Disable the account.
usr.SetInfo

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="example-2"></a><span data-ttu-id="7ab7a-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="7ab7a-110">Example 2</span></span>

<span data-ttu-id="7ab7a-111">下列程式碼範例示範如何使用 c + + 搭配 ADSI 來停用帳戶。</span><span class="sxs-lookup"><span data-stu-id="7ab7a-111">The following code example shows how to disable an account using C++ with ADSI.</span></span>


```C++
IADsUser *pUser;

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath=L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->put_AccountDisabled(TRUE);
hr = pUser->SetInfo();
```



 

 




