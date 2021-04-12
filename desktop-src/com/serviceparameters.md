---
title: ServiceParameters
description: 指定要傳遞至物件的命令列參數，這些參數會透過 LocalService 登錄值傳遞給已安裝供 COM 使用的物件。
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- ServiceParameters 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300960"
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

 

 




