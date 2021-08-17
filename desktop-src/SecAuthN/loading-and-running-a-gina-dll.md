---
description: Windows 載入並執行標準的 Microsoft GINA DLL (MSGina.dll) 。 若要載入不同的 GINA，您必須變更登錄機碼值。
ms.assetid: 408511af-4430-4dd7-a2a1-c32b375821c4
title: 載入和執行 GINA DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10a4e8d68a1e1846a28e1db9402d730834768a132a7c502021fd101f20926f54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140951"
---
# <a name="loading-and-running-a-gina-dll"></a>載入和執行 GINA DLL

Windows 載入並執行標準的 Microsoft GINA DLL (MSGina.dll) 。 若要載入不同的 [*GINA*](../secgloss/g-gly.md)，您必須變更下列登錄機碼值：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
                  GinaDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_SZ</dd>
</dl>
```

如果有 GinaDLL 機碼值，它必須包含 [*Winlogon*](../secgloss/w-gly.md) 將載入和使用的 GINA DLL 名稱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立和測試 GINA DLL](building-and-testing-a-gina-dll.md)
</dt> <dt>

[GINA 匯出函數](authentication-functions.md)
</dt> <dt>

[GINA 結構](authentication-structures.md)
</dt> <dt>

[終端機服務 GINA 函式](terminal-services-gina-functions.md)
</dt> </dl>

 

 
