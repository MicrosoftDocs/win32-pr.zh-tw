---
title: TlsServerUseAllPurposeCert
description: TlsServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證來進行 EAP-TLS 驗證。
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313814"
---
# <a name="tlsserveruseallpurposecert"></a>TlsServerUseAllPurposeCert

TlsServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證來進行 EAP-TLS 驗證。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值        | 描述                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| 1            | 用戶端或伺服器憑證存儲中的所有用途憑證都是針對 PEAP 驗證所選取。     |
| 其他值 | 用戶端或伺服器憑證存儲中的所有用途憑證都不會針對 PEAP 驗證進行選取。 |



 

如果此登錄值不存在，則會選取用戶端或伺服器憑證存儲中的所有用途憑證以進行 EAP-TLS 驗證。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 登錄設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




