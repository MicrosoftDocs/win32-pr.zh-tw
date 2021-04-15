---
title: AssumePhase2Fragmentation
description: AssumePhase2Fragmentation 登錄機碼會判斷伺服器和用戶端是否採用階段2片段。
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104373991"
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

[EAPHost 登錄設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




