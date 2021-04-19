---
title: '使用者必須在下次登入時變更密碼 (WinNT 提供者) '
description: 若要啟用此選項，請將使用者的 PasswordExpired 屬性設定為一個 (1) 。 將此屬性設定為零 (0) 可讓使用者登入，而不需要變更密碼。
ms.assetid: 97dd4232-dcd3-44bd-8a2a-1dcb0f85d53c
ms.tgt_platform: multiple
keywords:
- 使用者必須在下次登入時變更密碼 (WinNT 提供者) ADSI
- 使用者必須在下次登入 ADSI、WinNT 提供者時變更密碼
- WinNT 提供者 ADSI、使用者管理範例、使用者必須在下次登入時變更密碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787be5f5f4e1534574a68c179bb699ac68c61e3e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "106976681"
---
# <a name="user-must-change-password-at-next-logon-winnt-provider"></a>使用者必須在下次登入時變更密碼 (WinNT 提供者) 

若要啟用此選項，請將使用者的 **PasswordExpired** 屬性設定為一個 (1) 。 將此屬性設定為零 (0) 可讓使用者登入，而不需要變更密碼。

## <a name="example-1"></a>範例 1

下列程式碼範例示範如何使用 Visual Basic 搭配 ADSI，在下一個登入選項上設定變更密碼。


```VB
Set usr = GetObject("WinNT://Fabrikam/jeffsmith,user")
usr.Put "PasswordExpired", CLng(1)   ' User must change password.
usr.SetInfo
```



## <a name="example-2"></a>範例 2

下列程式碼範例示範如何使用 c + + 搭配 ADSI，在下一次登入時設定變更密碼。


```C++
IADsUser *pUser = NULL;
HRESULT hr;

hr=ADsGetObject(L"WinNT://Fabrikam/jeffsmith,user",
                IID_IADsUser,
                (void**)&pUser);
VARIANT var;
VariantInit(&var);
V_I4(&var)=1;
V_VT(&var)=VT_I4;
hr = pUser->Put(_bstr_t("PasswordExpired"),var); // User must change password.
hr = pUser->SetInfo();

VariantClear(&var);
pUser->Release();
```



 

 




