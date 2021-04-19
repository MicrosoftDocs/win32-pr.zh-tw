---
title: 作業系統版本
description: 此 DWORD 資料類型應將作業系統類型保存為高序位單字，並將作業系統的版本號碼保留在低序位字組中。 下表列出作業系統的可能值。
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- 作業系統版本結構化儲存體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106978582"
---
# <a name="operating-system-versions"></a>作業系統版本

此 **DWORD** 資料類型應將作業系統類型保存為高序位單字，並將作業系統的版本號碼保留在低序位字組中。 下表列出作業系統的可能值。



| 作業系統       | 值  |
|------------------------|--------|
| 32位 Windows (Win32)  | 0x0002 |
| Macintosh              | 0x0001 |
| 16位 Windows (Win16)  | 0x0000 |



 

針對 Microsoft Windows 作業系統，作業系統版本是由 [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) 函數傳回的低序位文字。 針對 Microsoft Windows，下列範例程式碼會正確地設定來源作業系統的版本。

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 