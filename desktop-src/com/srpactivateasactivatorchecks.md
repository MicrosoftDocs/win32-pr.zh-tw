---
title: SRPActivateAsActivatorChecks
description: 判斷 ActivateAsActivator 啟用期間是否使用軟體限制原則 (SRP) 信任層級。
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- SRPActivateAsActivatorChecks 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672488"
---
# <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks

判斷 ActivateAsActivator 啟用期間是否使用軟體限制原則 (SRP) 信任層級。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值。

字串值 {N，N，NO，No，no} 表示伺服器物件會以用戶端物件的 SRP 信任層級執行，而不論其設定所在的 SRP 信任層級為何。 如果此登錄值設定為任何其他值或不存在，則為伺服器物件設定的 SRP 信任層級會與用戶端物件的 SRP 信任層級進行比較，並使用更嚴格的信任層級來執行伺服器物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




