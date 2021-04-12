---
title: 變更影片捕獲設定
description: 變更影片捕獲設定
ms.assetid: a5fe7e1e-084d-4102-91d4-ffe5d1d0e5c8
keywords:
- capCaptureGetSetup 宏
- capCaptureSetSetup 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b3f2629325c67bcad1fed26a9fed4d053372392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372594"
---
# <a name="changing-a-video-capture-setting"></a><span data-ttu-id="11464-105">變更影片捕獲設定</span><span class="sxs-lookup"><span data-stu-id="11464-105">Changing a Video Capture Setting</span></span>

<span data-ttu-id="11464-106">下列範例會使用 [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) 和 [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) 宏來變更預設值的捕獲速率 (每秒15個畫面格) 為每秒10個畫面格。</span><span class="sxs-lookup"><span data-stu-id="11464-106">The following example uses the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) and [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macros to change the capture rate from the default value (15 frames per second) to 10 frames per second.</span></span>


```C++
CAPTUREPARMS CaptureParms;
float FramesPerSec = 10.0;

capCaptureGetSetup(hWndC, &CaptureParms, sizeof(CAPTUREPARMS));

CaptureParms.dwRequestMicroSecPerFrame = (DWORD) (1.0e6 / 
    FramesPerSec);
capCaptureSetSetup(hWndC, &CaptureParms, sizeof (CAPTUREPARMS)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="11464-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="11464-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11464-108">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="11464-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




