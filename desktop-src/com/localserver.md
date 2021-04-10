---
title: LocalServer
description: 指定16位本機伺服器應用程式的完整路徑。
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- LocalServer 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021792"
---
# <a name="localserver"></a>LocalServer

指定16位本機伺服器應用程式的完整路徑。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a>備註

這是 **REG \_ SZ** 值，可指定完整路徑，而且可以包含任何命令列引數。

COM 會將 "-嵌入" 旗標附加至字串，因此使用旗標的應用程式必須剖析整個字串，並檢查內嵌旗標。

若要在不同的記憶體空間中執行 COM 物件伺服器，請變更 **LocalServer** 的值，如下所示：

**cmd/c 開始/separate** *路徑 * * * .exe**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**LocalServer32**](localserver32.md)
</dt> </dl>

 

 




