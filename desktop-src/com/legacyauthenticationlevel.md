---
title: LegacyAuthenticationLevel
description: 針對未呼叫 CoInitializeSecurity 的應用程式設定預設驗證層級。
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- LegacyAuthenticationLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022098"
---
# <a name="legacyauthenticationlevel"></a>LegacyAuthenticationLevel

針對未呼叫 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)的應用程式設定預設驗證層級。

> [!Caution]  
> 不建議您變更這個值，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。 如果您要變更此值，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。 如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。

 

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a>備註

這是 **REG \_ 單字** 值，相當於 RPC \_ C \_ 驗證 \_ 層級常數。



| 值 | 常數                             |
|-------|--------------------------------------|
| 1     | RPC \_ C \_ 驗證 \_ 層級 \_ 無           |
| 2     | RPC \_ C \_ 驗證 \_ LEVEL \_ CONNECT        |
| 3     | RPC \_ C \_ 驗證 \_ 層級 \_ 呼叫           |
| 4     | RPC \_ C \_ 驗證 \_ 層級 \_ PKT            |
| 5     | RPC \_ C \_ 驗證 \_ 層級 \_ PKT \_ 完整性 |
| 6     | RPC \_ C \_ 驗證 \_ LEVEL \_ PKT \_ 隱私權   |



 

如果此登錄值不存在，系統建立的預設驗證層級為 2 (RPC \_ C \_ 驗證 \_ CONNECT) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AuthenticationLevel**](authenticationlevel.md)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[設定整個進程的安全性](setting-processwide-security.md)
</dt> </dl>

 

 




