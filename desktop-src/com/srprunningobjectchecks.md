---
title: SRPRunningObjectChecks
description: 決定是否要針對相容的軟體限制原則（ (SRP) 信任層級）篩選連接到執行中物件的嘗試。
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- SRPRunningObjectChecks 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672487"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

決定是否要針對相容的軟體限制原則（ (SRP) 信任層級）篩選連接到執行中物件的嘗試。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值。

字串值 {N，N，NO，No，no} 表示不會針對相容的 SRP 信任層級篩選連接到執行物件的嘗試。 如果此登錄值設定為任何其他值或不存在，則執行中的物件不能有比用戶端物件更嚴格的 SRP 信任層級。 例如，如果用戶端物件具有不受限制的信任層級，則執行中的物件不能有不允許的信任層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




