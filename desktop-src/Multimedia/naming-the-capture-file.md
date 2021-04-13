---
title: 命名捕獲檔案
description: 命名捕獲檔案
ms.assetid: fae2fd6a-4c2f-432f-a714-9faae6daeafe
keywords:
- capFileSetCaptureFile 宏
- capFileAlloc 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ea091a36777e176124689ba57be6c0fb75d07d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301223"
---
# <a name="naming-the-capture-file"></a><span data-ttu-id="8660d-105">命名捕獲檔案</span><span class="sxs-lookup"><span data-stu-id="8660d-105">Naming the Capture File</span></span>

<span data-ttu-id="8660d-106">下列範例會使用 [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) 宏來指定 capture 檔 (MYCAP.AVI) 的替代檔案名，並使用 [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) 宏來預先配置 5 MB 的檔案。</span><span class="sxs-lookup"><span data-stu-id="8660d-106">The following example uses the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro to specify an alternate filename (MYCAP.AVI) for the capture file and the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro to preallocate a file of 5 MB.</span></span>


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a><span data-ttu-id="8660d-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="8660d-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8660d-108">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="8660d-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




