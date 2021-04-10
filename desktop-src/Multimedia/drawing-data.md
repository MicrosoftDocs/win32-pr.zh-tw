---
title: 繪製資料
description: 繪製資料
ms.assetid: cc4f383d-54d4-4027-ad6a-da19bb07c17f
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) 、繪圖
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，繪圖
- ICDraw 函式
- ICDrawStart 宏
- ICDrawStop 宏
- ICDrawFlush 宏
- ICDrawEnd 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f598ef47bbbf6b8f53c7fb2639c9ddff1390ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021203"
---
# <a name="drawing-data"></a>繪製資料

下列範例會使用 [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) 函式和 [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart)、 [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop)、 [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush)和 [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) 宏來繪製螢幕上的資料。


```C++
DWORD    dwNumBuffers; 
 
// Find out how many buffers need filling before drawing starts.

ICGetBuffersWanted(hIC, &dwNumBuffers); 
for (dw = 0; dw < dwNumBuffers; dw++)
{ 
    ICDraw(hIC, 0, lpFormat, lpData, cbData, dw); // fill the pipeline
    
    // Point lpFormat and lpData to next format and buffer.
    
} 
ICDrawStart(hIC);  // starts the clock 
dw = 0; 
while (fPlaying) 
{ 
    ICDraw(hIC, 0, lpFormat, lpData, chData, dw); // fill more buffers 
    
    // Point lpFormat and lpData to next format and buffer,
    // update dw.
} 
 
ICDrawStop(hIC);   // stops drawing and decompressing when done 
ICDrawFlush(hIC);  // flushes any existing buffers 
ICDrawEnd(hIC);    // ends decompression 
 
```



 

 




