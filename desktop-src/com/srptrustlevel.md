---
title: SRPTrustLevel
description: 將軟體限制原則設定 (SRP) 信任層級的應用程式。
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- SRPTrustLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c1e9290cbe04cfe33e1192b95b86ca03fd5ea5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372027"
---
# <a name="srptrustlevel"></a>SRPTrustLevel

將軟體限制原則設定 (SRP) 信任層級的應用程式。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      SRPTrustLevel = value
```

## <a name="remarks"></a>備註

這是從 Windows XP 開始提供的 **REG \_ DWORD** 值。



| 值                                 | 描述                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------|
| 0x0 (更安全的 \_ LEVELID 不 \_ 允許)       | 不允許應用程式存取和安全性敏感的使用者權限。 |
| 0x40000 (SAFE \_ LEVELID \_ FULLYTRUSTED)  | 應用程式可不受限制地存取使用者的許可權。                    |



 

如果 **SRPTrustLevel** 值不存在， \_ \_ 就會使用 [不允許的安全 LEVELID] 的預設值。 如果 **SRPTrustLevel** 的類型錯誤或超出範圍，COM 會傳回錯誤 COMADMIN \_ E \_ SAFERINVALID。 如果任何排序的啟用因為 SRP 信任檢查而失敗，COM 會傳回錯誤共同的 \_ E \_ ACTI加值稅IONFAILED。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的安全性](security-in-com.md)
</dt> <dt>

[**SRPActivateAsActivatorChecks**](srpactivateasactivatorchecks.md)
</dt> <dt>

[**SRPRunningObjectChecks**](srprunningobjectchecks.md)
</dt> </dl>

 

 




