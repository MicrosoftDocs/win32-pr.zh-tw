---
title: " (WinNT 提供者的帳戶到期) "
description: 使用 WinNT 提供者時，您可以使用 IADsUser. Iadsuser.accountexpirationdate 屬性來設定帳戶到期日。
ms.assetid: 1d887a33-a3ae-4c61-88fa-2764a6bbf6bf
ms.tgt_platform: multiple
keywords:
- 帳戶到期 ADSI，WinNT 提供者
- WinNT 提供者 ADSI，使用者管理範例，帳戶到期日
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4936004cbd68c853f5e6d5c76a405f2a8340d22a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106974825"
---
# <a name="account-expiration-winnt-provider"></a><span data-ttu-id="4e0e7-105"> (WinNT 提供者的帳戶到期) </span><span class="sxs-lookup"><span data-stu-id="4e0e7-105">Account Expiration (WinNT Provider)</span></span>

<span data-ttu-id="4e0e7-106">使用 WinNT 提供者時，您可以使用 [**IADsUser. iadsuser.accountexpirationdate**](iadsuser-property-methods.md) 屬性來設定帳戶到期日。</span><span class="sxs-lookup"><span data-stu-id="4e0e7-106">When using the WinNT provider, the account expiration date can be set using the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property.</span></span>

<span data-ttu-id="4e0e7-107">若要設定帳戶到期日，請將 [**IADsUser. iadsuser.accountexpirationdate**](iadsuser-property-methods.md) 屬性設定為所需的日期值。</span><span class="sxs-lookup"><span data-stu-id="4e0e7-107">To set the account expiration date, set the [**IADsUser.AccountExpirationDate**](iadsuser-property-methods.md) property to the desired date value.</span></span> <span data-ttu-id="4e0e7-108">若要將帳戶到期日設為永不過期，請將此屬性設定為「1970年1月1日」。</span><span class="sxs-lookup"><span data-stu-id="4e0e7-108">To set the account expiration date to never expire, set this property to "January 1, 1970".</span></span>

## <a name="example-1"></a><span data-ttu-id="4e0e7-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="4e0e7-109">Example 1</span></span>

<span data-ttu-id="4e0e7-110">下列程式碼範例示範如何使用 Visual Basic 搭配 ADSI 來設定帳戶到期日。</span><span class="sxs-lookup"><span data-stu-id="4e0e7-110">The following code example shows how to set the account expiration date using Visual Basic with ADSI.</span></span>


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a><span data-ttu-id="4e0e7-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="4e0e7-111">Example 2</span></span>

<span data-ttu-id="4e0e7-112">下列程式碼範例示範如何使用 c + + 和 ADSI 來設定帳戶到期日。</span><span class="sxs-lookup"><span data-stu-id="4e0e7-112">The following code example shows how to set the account expiration date using C++ with ADSI.</span></span>


```C++
void SetUserAccountExpirationDate(IADsUser *pUser, DATE date)
{
   if(!pUser) return;

   HRESULT hr = S_OK;
   hr = pUser->put_AccountExpirationDate(date); // Set the account to expires on date.
   
   hr = pUser->SetInfo();
   hr = pUser->Release();
   return;
}
```



 

 




