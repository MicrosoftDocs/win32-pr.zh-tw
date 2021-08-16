---
title: DoNotAddAllApplicationPackagesToRestrictions
description: 判斷依預設，RPCSS 是否會自動 \_ 將所有應用程式 \_ 封裝 SID 附加至 COM 限制。
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1608d49d7e5bebc977ace8e59e4b31c5b13da8ab4f743e89095b9f31632453c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737004"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a>DoNotAddAllApplicationPackagesToRestrictions

判斷依預設，RPCSS 是否會自動 \_ 將所有應用程式 \_ 封裝 SID 附加至 COM 限制。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值 | 描述                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| 0     | 從 Windows 7 遷移到 Windows 8 時，停用 Windows 存放區應用程式。                   |
| 1     | 不會將所有 \_ 應用程式 \_ 封裝 SID 新增至 COM 限制。 此為預設值。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




