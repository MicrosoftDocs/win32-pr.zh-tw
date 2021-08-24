---
title: EnableDCOM
description: 控制電腦的全域啟用和呼叫原則。 只有系統管理員和系統才能完整存取登錄的這個部分。 所有其他使用者都具有唯讀存取權。
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- EnableDCOM 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74aea79cf600aad4407b96b5c4a10e8f44633a1c928f8b7e376c192b108cb75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793597"
---
# <a name="enabledcom"></a>EnableDCOM

控制電腦的全域啟用和呼叫原則。 只有系統管理員和系統才能完整存取登錄的這個部分。 所有其他使用者都具有唯讀存取權。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值。



| 值    | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| N (或 n)  | 沒有任何遠端用戶端可以啟動伺服器或連接到這部電腦上的物件。 本機用戶端無法存取遠端 DCOM 伺服器;封鎖所有 DCOM 流量。 根據類別的 [**LaunchPermission**](launchpermission.md) 登錄值和 global [**DefaultLaunchPermission**](defaultlaunchpermission.md) 登錄值的值和存取權限，每個類別都允許對類別程式碼的本機啟動，並連接到物件。 |
| Y (或 y)  | 根據類別的 [**LaunchPermission**](launchpermission.md) 登錄值和 global [**DefaultLaunchPermission**](defaultlaunchpermission.md) 登錄值的值和存取權限，每個類別都允許啟動伺服器並連接至物件。                                                                                                                                                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




