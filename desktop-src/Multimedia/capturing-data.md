---
title: 捕獲資料
description: 捕獲資料
ms.assetid: de029673-9929-40f9-b29b-2598e1e5c988
keywords:
- capCaptureSequence 宏
- capFileSaveAs 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24b2110da9a85faaa991e67efdd1ef48e3d9c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021802"
---
# <a name="capturing-data"></a><span data-ttu-id="aeebf-105">捕獲資料</span><span class="sxs-lookup"><span data-stu-id="aeebf-105">Capturing Data</span></span>

<span data-ttu-id="aeebf-106">下列範例會使用 [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) 宏啟動影片捕獲，並使用 [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) 宏將捕獲的資料從 capture 檔案複製到檔案 NEWFILE.AVI。</span><span class="sxs-lookup"><span data-stu-id="aeebf-106">The following example uses the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro to start video capture and the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro to copy the captured data from the capture file to the file NEWFILE.AVI.</span></span>


```C++
char szNewName[] = "NEWFILE.AVI";

// Set up the capture operation.

capCaptureSequence(hWndC); 

// Capture.

capFileSaveAs(hWndC, szNewName); 
 
```



## <a name="related-topics"></a><span data-ttu-id="aeebf-107">相關主題</span><span class="sxs-lookup"><span data-stu-id="aeebf-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aeebf-108">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="aeebf-108">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




