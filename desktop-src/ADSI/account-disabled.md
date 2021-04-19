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
ms.openlocfilehash: 3e61fb65a06f4e2afb1b43595b955c577b2a6090
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106975644"
---
# <a name="account-disabled-ldap-provider"></a><span data-ttu-id="99f53-107">帳戶已停用 (LDAP 提供者) </span><span class="sxs-lookup"><span data-stu-id="99f53-107">Account Disabled (LDAP Provider)</span></span>

<span data-ttu-id="99f53-108">若要停用使用者帳戶，請在 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)介面中將 AccountDisabled 屬性設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="99f53-108">To disable a user account, set the AccountDisabled property to **TRUE** in the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span> <span data-ttu-id="99f53-109">這類似于 WinNT 提供者。</span><span class="sxs-lookup"><span data-stu-id="99f53-109">This is similar to the WinNT provider.</span></span> <span data-ttu-id="99f53-110">下列程式碼範例示範如何停用使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="99f53-110">The following code examples show how to disable a user account.</span></span>

## <a name="example-1"></a><span data-ttu-id="99f53-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="99f53-111">Example 1</span></span>


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



## <a name="example-2"></a><span data-ttu-id="99f53-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="99f53-112">Example 2</span></span>


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



 

 




