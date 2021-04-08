---
title: 'Shell (COM) '
description: 提供 Windows 3.1 shell 列印和檔案開啟資訊。
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Shell 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685369"
---
# <a name="shell-com"></a>Shell (COM) 

提供 Windows 3.1 shell 列印和檔案 **開啟** 資訊。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a>備註

這些專案應該提供應用程式的路徑和檔案名。

 

 




