---
title: SRPRunningObjectChecks
description: 決定是否要針對相容的軟體限制原則（ (SRP) 信任層級）篩選連接到執行中物件的嘗試。
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- SRPRunningObjectChecks 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c416b5f430540282873e37c5e74ef2cccc1c564f4a5b27842ba2a49e99cc8769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129790"
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

 

 




