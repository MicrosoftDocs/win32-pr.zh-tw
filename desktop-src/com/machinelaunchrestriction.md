---
title: MachineLaunchRestriction
description: 設定元件啟動和啟用的全電腦限制原則。
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- MachineLaunchRestriction 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5cd235e2dd81e596448f25adfd72ad0b16c13d2da3860eb56fb95f93ef53cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048056"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

設定元件啟動和啟用的全電腦限制原則。

> [!Caution]  
> 變更這個值將會影響所有的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。 如果有 COM 伺服器應用程式的限制低於全電腦限制，則減少整個電腦的限制可能會將這些應用程式公開給不必要的存取。 相反地，如果您增加全電腦的限制，則呼叫應用程式可能無法再存取某些 COM 伺服器應用程式。

 

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>備註

這是 **REG \_ 二進位** 值。

如果主體未授與許可權，則無法取得它們，即使許可權是由 [DefaultAccessPermission](defaultaccesspermission.md) 登錄值或 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數授與。

依預設，系統管理員可以取得本機和遠端啟動和啟用許可權，而 Everyone 群組的成員可能會取得本機啟用和啟動許可權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




