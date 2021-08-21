---
title: PeapServerUseAllPurposeCert
description: PeapServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證進行 PEAP 驗證。
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5086a0067bab70a0e222def34d1adf236b37127c0d1ff6c91ac83b8b28c73c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042816"
---
# <a name="peapserveruseallpurposecert"></a>PeapServerUseAllPurposeCert

PeapServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證進行 PEAP 驗證。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值        | 描述                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | 用戶端或伺服器憑證存儲中的所有用途憑證都是針對 PEAP 驗證所選取。     |
| 其他值 | 用戶端或伺服器憑證存儲中的所有用途憑證都不會針對 PEAP 驗證進行選取。 |



 

如果此登錄值不存在，則會選取用戶端或伺服器憑證存儲中的所有用途憑證進行 PEAP 驗證。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost Registry 設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




