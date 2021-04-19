---
title: DefaultLaunchPermission
description: 定義存取控制清單 (ACL) 可啟動的類別，這些類別無法透過 LaunchPermission 登錄值指定自己的 ACL。
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- DefaultLaunchPermission 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966829"
---
# <a name="defaultlaunchpermission"></a>DefaultLaunchPermission

定義存取控制清單 (ACL) 可啟動的類別，這些類別無法透過 [**LaunchPermission**](launchpermission.md) 登錄值指定自己的 ACL。

> [!Caution]  
> 不建議您變更這個值，因為這會影響所有未設定整個進程安全性的 COM 伺服器應用程式，而且可能會讓它們無法正常運作。 如果您要變更此值，以影響特定 COM 應用程式的安全性設定，您應該改為變更該特定 COM 應用程式的整個進程安全性設定。 如需設定整個進程安全性的詳細資訊，請參閱 [設定整個進程的安全性](setting-processwide-security.md)。

 

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a>備註

這是 **REG \_ 二進位** 值。

預設存取權限如下所示：

-   系統管理員：允許啟動
-   系統：允許啟動
-   互動式：允許啟動

如果為伺服器設定 [**LaunchPermission**](launchpermission.md) 值，其優先順序會高於 **DefaultLaunchPermission** 值。 當您收到本機或遠端要求以啟動伺服器，其 [**AppID**](appid-key.md) 金鑰本身沒有 **LaunchPermission** 值時，會在模擬用戶端時檢查此值所描述的 ACL，而其成功允許或不允許啟動類別程式碼。

此值提供簡單的集中式系統管理層級，讓您在電腦上以其他方式 unadministered 類別來啟動存取。 例如，系統管理員可能會使用 DCOMCNFG 工具來設定系統，以允許 Power Users 的唯讀存取。 因此，OLE 會限制對 Power Users 群組的成員啟動類別程式碼的要求。 系統管理員接著可以設定個別類別的啟動許可權，以將啟動類別程式碼的能力授與其他群組或個別使用者（如有需要）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**LaunchPermission**](launchpermission.md)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> <dt>

[設定整個進程的安全性](setting-processwide-security.md)
</dt> </dl>

 

 




