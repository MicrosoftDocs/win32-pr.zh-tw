---
title: DoNotAddAllApplicationPackagesToRestrictions
description: 判斷依預設，RPCSS 是否會自動 \_ 將所有應用程式 \_ 封裝 SID 附加至 COM 限制。
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371916"
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
| 0     | 從 Windows 7 遷移至 Windows 8 時停用 Windows Store 應用程式。                   |
| 1     | 不會將所有 \_ 應用程式 \_ 封裝 SID 新增至 COM 限制。 此為預設值。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




