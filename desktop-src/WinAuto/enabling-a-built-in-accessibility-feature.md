---
title: 啟用內建協助工具功能
ms.assetid: f97a445d-f93d-4462-bce5-d853f5076b9c
description: 深入瞭解：啟用內建協助工具功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d860b1410e48f5824923b8b16babb6bcd1527ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195564"
---
# <a name="enabling-a-built-in-accessibility-feature"></a>啟用內建協助工具功能

下列程式碼片段會使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函數來啟用篩選篩選功能：


```C++
FILTERKEYS fk; 
BOOL bSuccess; 
 
// Fill in the members of the FILTERKEYS structure.  
 
fk.cbSize = sizeof(FILTERKEYS); 
fk.dwFlags = (FKF_FILTERKEYSON | FKF_HOTKEYACTIVE | 
                       FKF_AVAILABLE | FKF_HOTKEYSOUND |
FKF_CLICKON); 
fk.iWaitMSec = 1000; 
fk.iDelayMSec = 1000; 
fk.iRepeatMSec = 500; 
fk.iBounceMSec = 0; 
 
// Call SystemParametersInfo with the SPI_SETFILTERKEYS flag.  
 
bSuccess = SystemParametersInfo(SPI_SETFILTERKEYS, 0, (LPVOID)
&fk, 0); 
```



 

 
