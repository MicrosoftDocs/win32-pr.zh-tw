---
title: 控制
description: 將物件識別為 ActiveX 控制項。
ms.assetid: 2487e642-1d21-4811-87dd-b280be98a44b
keywords:
- 控制登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03aa6a0b131dd5fc2ba10d9aaeabafd06b19b73bb1e9422c28e5bec45ea43cbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120508"
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

 

 




