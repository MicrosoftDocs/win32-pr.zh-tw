---
title: ServiceParameters
description: 指定要傳遞至物件的命令列參數，這些參數會透過 LocalService 登錄值傳遞給已安裝供 COM 使用的物件。
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- ServiceParameters 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103b55269b700beaf5c85e3408e3597e63fb9140e4dc79fe4bb895ff6767bfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129960"
---
# <a name="serviceparameters"></a>ServiceParameters

指定要傳遞至物件的命令列參數，這些參數會透過 [**LocalService**](localservice.md) 登錄值傳遞給已安裝供 COM 使用的物件。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值。 在啟動時，此字串會以命令列引數的形式傳遞給服務。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**LocalService**](localservice.md)
</dt> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> </dl>

 

 




