---
title: BypassNegotiation
description: BypassNegotiation 登錄機碼會判斷伺服器和用戶端之間是否有功能協商，或是否使用預先設定的設定。
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104374027"
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

[EAPHost 登錄設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




