---
title: BypassNegotiation
description: BypassNegotiation 登錄機碼會判斷伺服器和用戶端之間是否有功能協商，或是否使用預先設定的設定。
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ba914b9c1ec1d5e3caef6b86ddbda49d021268e456c877ff4f67db86efd2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978248"
---
# <a name="bypassnegotiation"></a>BypassNegotiation

BypassNegotiation 登錄機碼會判斷伺服器和用戶端之間是否有功能協商，或是否使用預先設定的設定。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值   | 描述                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0       | 伺服器和用戶端會協商 EAP 功能。                                                                                                                                                        |
| 零 | 伺服器和用戶端不會協調 EAP 功能。 伺服器和用戶端會使用 [AssumePhase2Fragmentation](assumephase2fragmentation.md) 登錄機碼值來尋找另一方的功能。 |



 

如果此登錄值不存在，伺服器和用戶端會協商 EAP 功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost Registry 設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




