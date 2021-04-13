---
title: InvalidSecurityDescriptorLoggingLevel
description: 針對元件啟動和存取權限的無效安全描述項，設定事件記錄檔專案的詳細資訊。
ms.assetid: 44f680b8-083d-44f0-a353-e66b87787ab7
keywords:
- InvalidSecurityDescriptorLoggingLevel 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ac333a7cb8b54f383f93a71131cbb0a9314466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300019"
---
# <a name="invalidsecuritydescriptorlogginglevel"></a>InvalidSecurityDescriptorLoggingLevel

針對元件啟動和存取權限的無效安全描述項，設定事件記錄檔專案的詳細資訊。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   InvalidSecurityDescriptorLoggingLevel = value
```

## <a name="remarks"></a>備註

這是 **REG \_ DWORD** 值。



| 值 | 描述                                                                                                                                                                    |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | 當 COM 找到不正確安全描述項時，一律會記錄失敗。 這是預設值。                                                                                  |
| 2     | 當 COM 找不到不正確安全描述項時，永遠不會記錄失敗。 不建議您停用事件記錄，因為它可以讓您更難診斷問題。 |



 

如果您將啟動和存取權限安全描述項 (通常稱為 Acl) 直接，則可以建立其意義無法明確解讀的安全描述項。 當 COM 遇到這類不正確安全描述項時，會產生事件記錄檔專案。

請注意， [**ActivationFailureLoggingLevel**](activationfailurelogginglevel.md) 和 [**CallFailureLoggingLevel**](callfailurelogginglevel.md) 無法控制記錄不正確安全描述項錯誤。 使用 **InvalidSecurityDescriptorLoggingLevel** 可完整控制此功能。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 COM 應用程式的安全性](setting-security-for-com-applications.md)
</dt> </dl>

 

 




