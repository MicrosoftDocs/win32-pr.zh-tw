---
title: 列舉已安裝的 Capture 驅動程式
description: 列舉已安裝的 Capture 驅動程式
ms.assetid: 3a70bf5b-1e0a-48d3-aa6b-be66692f0400
keywords:
- capGetDriverDescription 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8fe85103259354bcc3b42834ecaff03d660eb408cda8191e5e0abea7393d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988647"
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

 

 




