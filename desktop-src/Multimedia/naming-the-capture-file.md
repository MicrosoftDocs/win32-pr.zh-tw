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
# <a name="naming-the-capture-file"></a>命名捕獲檔案

下列範例會使用 [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) 宏來指定 capture 檔 (MYCAP.AVI) 的替代檔案名，並使用 [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) 宏來預先配置 5 MB 的檔案。


```C++
char szCaptureFile[] = "MYCAP.AVI";

capFileSetCaptureFile( hWndC, szCaptureFile); 
capFileAlloc( hWndC, (1024L * 1024L * 5)); 
 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用影片捕獲](using-video-capture.md)
</dt> </dl>

 

 




