---
title: 控制
description: 將物件識別為 ActiveX 控制項。
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- 控制登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3722d85b38399d7e95f226749bda45ccc82d1369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372631"
---
# <a name="control"></a>控制

將物件識別為 ActiveX 控制項。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Control
```

## <a name="remarks"></a>備註

容器會使用這個選擇性專案來填滿對話方塊。 容器會使用這個子機碼來判斷是否要在顯示 ActiveX 控制項的對話方塊中包含物件。 如果控制項設計成隻能搭配特定容器運作，因此不適合插入其他容器中，則控制項可以省略此專案。

 

 




