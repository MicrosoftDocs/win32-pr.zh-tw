---
title: MachineAccessRestriction
description: 針對元件存取設定整個電腦的限制原則。
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- MachineAccessRestriction 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966813"
---
# <a name="machineaccessrestriction"></a>MachineAccessRestriction

針對元件存取設定整個電腦的限制原則。

> [!Caution]  
> 變更這個值將會影響所有的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。 如果有 COM 伺服器應用程式的限制低於全電腦限制，則減少整個電腦的限制可能會將這些應用程式公開給不必要的存取。 相反地，如果您增加全電腦的限制，則呼叫應用程式可能無法再存取某些 COM 伺服器應用程式。

 

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>備註

這是 **REG \_ 二進位** 值。

如果主體未授與許可權，則無法取得它們，即使許可權是由 [DefaultAccessPermission](defaultaccesspermission.md) 登錄值或 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 函數授與。

依預設，Everyone 群組的成員可以取得本機和遠端存取許可權，而且匿名使用者可以取得本機存取權限。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




