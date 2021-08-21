---
title: SRPTrustLevel
description: 將軟體限制原則設定 (SRP) 信任層級的應用程式。
ms.assetid: 2ec10eb5-f83a-4ce7-8e03-36cdafadf169
keywords:
- SRPTrustLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b348f4159939342693cf4da4af0aacd71d030159ddcd992008d1fde71fd7bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104178"
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

 

 




