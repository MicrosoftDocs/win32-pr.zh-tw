---
title: 啟用影片重迭
description: 啟用影片重迭
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- capDriverGetCaps 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce51a3b7c77fbb161007ddde7dfe91c36152121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675271"
---
# <a name="enabling-video-overlay"></a><span data-ttu-id="5ec38-104">啟用影片重迭</span><span class="sxs-lookup"><span data-stu-id="5ec38-104">Enabling Video Overlay</span></span>

<span data-ttu-id="5ec38-105">下列範例會使用 [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) 宏來判斷 capture 驅動程式是否有重迭的功能;如果有的話，宏會啟用覆迭。</span><span class="sxs-lookup"><span data-stu-id="5ec38-105">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to determine whether a capture driver has overlay capabilities; if it does, the macro enables the overlay.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 

if (CapDrvCaps.fHasOverlay) 
    capOverlay(hWndC, TRUE);
 
```



## <a name="related-topics"></a><span data-ttu-id="5ec38-106">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ec38-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec38-107">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="5ec38-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




