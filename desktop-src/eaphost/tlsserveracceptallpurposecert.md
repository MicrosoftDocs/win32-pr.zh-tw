---
title: TlsServerAcceptAllPurposeCert
description: TlsServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 EAP-TLS 驗證的所有用途憑證。
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106966228"
---
# <a name="tlsserveracceptallpurposecert"></a>TlsServerAcceptAllPurposeCert

TlsServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 EAP-TLS 驗證的所有用途憑證。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值        | 描述                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| 1            | 伺服器和用戶端接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證。       |
| 其他值 | 伺服器和用戶端不接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證 |



 

如果此登錄值不存在，伺服器和用戶端會接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost 登錄設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




