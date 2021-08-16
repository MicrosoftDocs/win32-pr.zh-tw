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
ms.openlocfilehash: 4fd23973a4de31fed629428be9f4df1b6cade34e77f78680a5f87c9d55c42234
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838408"
---
# <a name="account-expiration-winnt-provider"></a> (WinNT 提供者的帳戶到期) 

使用 WinNT 提供者時，您可以使用 [**IADsUser. iadsuser.accountexpirationdate**](iadsuser-property-methods.md) 屬性來設定帳戶到期日。

若要設定帳戶到期日，請將 [**IADsUser. iadsuser.accountexpirationdate**](iadsuser-property-methods.md) 屬性設定為所需的日期值。 若要將帳戶到期日設為永不過期，請將此屬性設定為「1970年1月1日」。

## <a name="example-1"></a>範例 1

下列程式碼範例示範如何使用 Visual Basic 搭配 ADSI 來設定帳戶到期日。


```VB
Dim usr As IADsUser

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
usr.AccountExpirationDate = "05/06/1998"
usr.SetInfo
 
' Set the account to never expire.
usr.AccountExpirationDate = "01/01/1970"
usr.SetInfo
```



## <a name="example-2"></a>範例 2

下列程式碼範例示範如何使用 c + + 和 ADSI 來設定帳戶到期日。


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



 

 




