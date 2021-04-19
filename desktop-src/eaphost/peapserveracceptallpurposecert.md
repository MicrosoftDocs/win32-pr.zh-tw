---
title: PeapServerAcceptAllPurposeCert
description: PeapServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 PEAP 驗證的所有用途憑證。
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106969089"
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

[EAPHost 登錄設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




