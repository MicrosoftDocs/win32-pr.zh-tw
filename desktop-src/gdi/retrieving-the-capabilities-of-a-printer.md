---
description: 並非每個輸出裝置都支援整個圖形功能集。
ms.assetid: 7989d393-7be4-47fc-af8d-26dd549c48be
title: 取出印表機的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d84db8d46255f4dfd33ce62ab4ab6735b0f2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972521"
---
# <a name="retrieving-the-capabilities-of-a-printer"></a><span data-ttu-id="f04d2-103">取出印表機的功能</span><span class="sxs-lookup"><span data-stu-id="f04d2-103">Retrieving the Capabilities of a Printer</span></span>

<span data-ttu-id="f04d2-104">並非每個輸出裝置都支援整個圖形功能集。</span><span class="sxs-lookup"><span data-stu-id="f04d2-104">Not every output device supports the entire set of graphics functions.</span></span> <span data-ttu-id="f04d2-105">例如，由於硬體限制，大部分的向量繪圖器都不支援位區塊傳輸。</span><span class="sxs-lookup"><span data-stu-id="f04d2-105">For example, because of hardware limitations, most vector plotters do not support bit-block transfers.</span></span> <span data-ttu-id="f04d2-106">應用程式可以藉由呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) 函式、指定適當的索引，以及檢查傳回值，來判斷裝置是否支援特定的圖形函式。</span><span class="sxs-lookup"><span data-stu-id="f04d2-106">An application can determine whether a device supports a particular graphics function by calling the [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function, specifying the appropriate index, and examining the return value.</span></span>

<span data-ttu-id="f04d2-107">下列範例顯示應用程式如何測試印表機，以判斷它是否支援位區塊傳輸。</span><span class="sxs-lookup"><span data-stu-id="f04d2-107">The following example shows how an application tests a printer to determine whether it supports bit-block transfers.</span></span>


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



 

 



