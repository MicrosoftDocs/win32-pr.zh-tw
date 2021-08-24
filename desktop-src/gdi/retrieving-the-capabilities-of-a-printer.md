---
description: 並非每個輸出裝置都支援整個圖形功能集。
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: 取出印表機的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c332832efc62f28ee77a5476ef12f706eb2e97a2cd5e86877e4a71a48feb907
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779058"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a>取出印表機的功能

並非每個輸出裝置都支援整個圖形功能集。 例如，由於硬體限制，大部分的向量繪圖器都不支援位區塊傳輸。 應用程式可以藉由呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式、指定適當的索引，以及檢查傳回值，來判斷裝置是否支援特定的圖形函式。

下列範例顯示應用程式如何測試印表機，以判斷它是否支援位區塊傳輸。


```C++
// Examine the raster capabilities of the device  
// identified by hdcPrint to verify that it supports  
// the BitBlt function.  
 
if ((GetDeviceCaps(hdcPrint, RASTERCAPS) 
       & RC_BITBLT) == 0) 
{ 
   DeleteDC(hdcPrint); 
   break; 
} 

else 
{ 
    // Print the bitmap using the printer DC.  
}
```



 

 



