---
title: '密碼永遠不會過期 (LDAP 提供者) '
description: 若要使用 LDAP 提供者啟用 [密碼永久有效] 選項，請在使用者的 userAccountControl 屬性中設定 ADS 的 [不會 \_ \_ \_ 過期 \_ PASSWD] 旗標。
ms.assetid: b8d7e7fe-c846-45c4-9c5f-770530453836
ms.tgt_platform: multiple
keywords:
- 密碼永遠不會過期 ADSI、LDAP 提供者
- LDAP 提供者 ADSI，使用者管理範例，密碼永遠不會到期
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa48145fa2b78c7685cdf52ab58b1e681df48c7d10a80f0ac7462fa7d4cb868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838928"
---
# <a name="password-never-expires-ldap-provider"></a>密碼永遠不會過期 (LDAP 提供者) 

若要使用 LDAP 提供者啟用 [密碼永久有效] 選項，請在使用者的 [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)屬性中設定 ADS 的 [不會 [**\_ \_ \_ 過期 \_ PASSWD**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum) ] 旗標。


```VB
Const ADS_UF_DONT_EXPIRE_PASSWD = &H10000

Set usr = GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=Com")
flag = usr.Get("userAccountControl")
newFlag = flag Or ADS_UF_DONT_EXPIRE_PASSWD
usr.Put "userAccountControl", newFlag
usr.SetInfo
```




```C++
#include <activeds.h>

IADsUser *pUser;
VARIANT var;
VariantInit(&var);

HRESULT hr = S_OK;
LPWSTR adsPath = L"LDAP://serv1/cn=Jeff Smith,cn=Users,dc=Fabrikam,dc=com";
hr = ADsGetObject(adsPath, IID_IADsUser, (void**)&pUser);

hr = pUser->Get(_bstr_t("userAccountControl"), &var);

V_I4(&var) |= ADS_UF_DONT_EXPIRE_PASSWD;
hr = pUser->Put(_bstr_t("userAccountControl"), var);

hr = pUser->SetInfo();
VariantClear(&var);
hr = pUser->Release();
```



 

 