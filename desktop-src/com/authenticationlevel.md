---
title: AuthenticationLevel
description: 針對未呼叫 CoInitializeSecurity 的應用程式，或針對呼叫 CoInitializeSecurity 並指定 AppID 的應用程式，設定驗證等級。
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- AuthenticationLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7968382ea97243c1116dd6785be34a0d1c3e6eafc6cb9ee13f16b939029a6611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120528"
---
# <a name="authenticationlevel"></a>AuthenticationLevel

針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 的應用程式，或針對呼叫 **CoInitializeSecurity** 並指定 AppID 的應用程式，設定驗證等級。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值，相當於 RPC \_ C \_ 驗證 \_ 層級常數。



| 值 | 常數                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ 驗證 \_ 層級 \_ 無           |
| 2     | RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT        |
| 3     | RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫           |
| 4     | RPC \_ C \_ 驗證 \_ 層級 \_ PKT            |
| 5     | RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性 |
| 6     | RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權   |



 

**AuthenticationLevel** 值類似于 [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)值。 如果有 **AuthenticationLevel** 值，就會使用它，而不是該 AppID 的 **LegacyAuthenticationLevel** 值。

如果 **AuthenticationLevel** 值的類型錯誤或超出範圍，則 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 會失敗，而導致介面封送處理失敗。 這可防止應用程式在所有 (跨單元、跨執行緒、跨進程或跨電腦) 進行任何呼叫。

**AuthenticationLevel** 和 [**AccessPermission**](accesspermission.md)值是獨立的。 如果不存在，則會使用預設值。 下列規則會列出 **AuthenticationLevel** 值與 **AccessPermission** 值之間的互動：

-   如果 **AuthenticationLevel** 為 NONE，則) 的應用程式 (會忽略 [**AccessPermission**](accesspermission.md) 和 [**DefaultAccessPermission**](defaultaccesspermission.md) 值。
-   如果 **AuthenticationLevel** 不存在，而且 [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) 為 NONE，則會忽略該應用程式)  (的 [**AccessPermission**](accesspermission.md) 和 [**DefaultAccessPermission**](defaultaccesspermission.md) 值。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[驗證層級常數](com-authentication-level-constants.md)
</dt> <dt>

[**LegacyAuthenticationLevel**](legacyauthenticationlevel.md)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




