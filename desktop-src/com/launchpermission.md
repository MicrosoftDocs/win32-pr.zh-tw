---
title: LaunchPermission
description: 描述可為此類別啟動新伺服器之主體 (ACL) 的存取控制清單。 此值可以在任何 AppID 金鑰下新增，以限制特定類別的遠端用戶端啟用。
ms.assetid: 7b8c1ae4-fbbd-489f-b1b5-60ae5a04f906
keywords:
- LaunchPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0e4c50568cae791f08b47fc44e10cc0d35fef07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022099"
---
# <a name="launchpermission"></a>LaunchPermission

描述可為此類別啟動新伺服器之主體 (ACL) 的存取控制清單。 此值可以在任何 [**AppID**](appid-key.md) 金鑰下新增，以限制特定類別的遠端用戶端啟用。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LaunchPermission = ACL
```

## <a name="remarks"></a>備註

這是 **REG \_ 二進位** 值。 在收到本機或遠端要求以啟動此類別的伺服器時，會在模擬用戶端時檢查此值所描述的 ACL，而且其成功允許或不允許啟動伺服器。 如果此值不存在，則會以相同的方式檢查 [**DefaultLaunchPermission**](defaultlaunchpermission.md) 值，以判斷是否可以啟動類別程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[**DefaultLaunchPermission**](defaultlaunchpermission.md)
</dt> <dt>

[COM 中的安全性](security-in-com.md)
</dt> </dl>

 

 




