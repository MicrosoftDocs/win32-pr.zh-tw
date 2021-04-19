---
title: " (WinNT 提供者，密碼永遠不會過期) "
description: 若要使用 WinNT ADSI 提供者來啟用此選項，請 \_ \_ \_ \_ 在 USERFLAGS 屬性上設定 ADS (0x10000) 旗標的 [不會讓 PASSWD 過期]。請注意，在 Windows 2000 和更新版本中，請使用 LDAP ADSI 提供者進行使用者管理作業，如下所示。
ms.assetid: 9e38b31c-399b-447f-bceb-36c599b2714e
ms.tgt_platform: multiple
keywords:
- " (WinNT 提供者，密碼永遠不會過期) "
- 密碼永遠不會過期 ADSI，WinNT 提供者
- WinNT 提供者 ADSI、使用者管理範例、密碼永遠不會到期
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343871e7ba8748b3e406f7c84a5a34c01a2793a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106999964"
---
# <a name="password-never-expires-winnt-provider"></a> (WinNT 提供者，密碼永遠不會過期) 

若要使用 WinNT ADSI 提供者來啟用此選項，請在 **UserFlags** 屬性上設定 ADS (0x10000) 旗標的 [不會讓 **\_ \_ \_ \_ PASSWD 過期**]。

> [!Note]  
> 若為 Windows 2000 和更新版本，請使用 LDAP ADSI 提供者進行使用者管理作業，如下所示。 如需詳細資訊，請參閱 [ (LDAP 提供者) 的密碼永不過期 ](password-never-expires.md)。

 

## <a name="example-1"></a>範例 1

下列程式碼範例示範如何搭配 ADSI 使用 Visual Basic 來設定 [密碼永久有效] 選項。


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000
Dim usr as IADs

Set usr = GetObject("WinNT://Fabrikam/JeffSmith")
oldFlags = usr.Get("UserFlags")
newFlags = oldFlags Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "UserFlags", newFlags
usr.SetInfo
```



## <a name="example-2"></a>範例 2

下列程式碼範例示範如何搭配使用 c + + 和 ADSI 來設定 [密碼永久有效] 選項。


```C++
#include <activeds.h>

IADsUser *pUser = NULL;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath;
adsPath = L"WinNT://Fabrikam/JeffSmith";
hr = ADsGetObject(adsPath,IID_IADsUser, (void**)&pUser);

CComBSTR sbstrUserFlags = "UserFlags";
hr = pUser->Get(sbstrUserFlags, &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(sbstrUserFlags, var);

hr = pUser->SetInfo();

VariantClear(&var);

pUser->Release();
```



 

 




