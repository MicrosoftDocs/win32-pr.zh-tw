---
title: 'Shell (COM) '
description: 提供 Windows 3.1 shell 列印和檔案開啟資訊。
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Shell 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ebbc83642896aa22f33b315e26097760f7311ec93d938cb0440a10e0aae049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129900"
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

 

 




