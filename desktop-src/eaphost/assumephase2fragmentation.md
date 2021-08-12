---
title: AssumePhase2Fragmentation
description: AssumePhase2Fragmentation 登錄機碼會判斷伺服器和用戶端是否採用階段2片段。
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caee785b0c89b92aaf4b01c590425c451b9a977664e915874e7eb5ad1edf46aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275835"
---
# <a name="assumephase2fragmentation"></a>AssumePhase2Fragmentation

AssumePhase2Fragmentation 登錄機碼會判斷伺服器和用戶端是否採用階段2片段。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值   | 描述                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| 0       | 伺服器和用戶端假設在 PEAP 驗證期間，另一方無法進行第2階段的片段。 |
| 零 | 伺服器和用戶端會假設另一方在 PEAP 驗證期間可以有階段2的片段。     |



 

如果此登錄值不存在，則伺服器和用戶端會假設另一個合作物件能夠在 PEAP 驗證期間進行階段2片段化。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost Registry 設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




