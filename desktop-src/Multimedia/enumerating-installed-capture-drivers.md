---
title: 列舉已安裝的 Capture 驅動程式
description: 列舉已安裝的 Capture 驅動程式
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- capGetDriverDescription 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a053b2de7a69a712914926dbd2ab72be9d1732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932313"
---
# <a name="enumerating-installed-capture-drivers"></a>列舉已安裝的 Capture 驅動程式

下列範例會使用 [**capGetDriverDescription**](/windows/desktop/api/Vfw/nf-vfw-capgetdriverdescriptiona) 函數來取得已安裝之 capture 驅動程式的名稱和版本。


```C++
char szDeviceName[80];
char szDeviceVersion[80];

for (wIndex = 0; wIndex < 10; wIndex++) 
{
    if (capGetDriverDescription(
            wIndex, 
            szDeviceName, 
            sizeof (szDeviceName), 
            szDeviceVersion, 
            sizeof (szDeviceVersion)
        )) 
    {
        // Append name to list of installed capture drivers
        // and then let the user select a driver to use.
    }
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 




