---
title: PeapServerAcceptAllPurposeCert
description: PeapServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 PEAP 驗證的所有用途憑證。
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d568ef2cf3e7fd5eeeaa650e5e6e4fd32a8e1c8d6baa0ed91434a5c0aa60ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118784680"
---
# <a name="peapserveracceptallpurposecert"></a>PeapServerAcceptAllPurposeCert

PeapServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 PEAP 驗證的所有用途憑證。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值        | 描述                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | 伺服器和用戶端接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證。       |
| 其他值 | 伺服器和用戶端不接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證 |



 

如果此登錄值不存在，伺服器和用戶端會接受由另一方針對 PEAP 驗證傳送的所有用途憑證。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost Registry 設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




