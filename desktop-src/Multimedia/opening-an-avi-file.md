---
title: 開啟 AVI 檔案
description: 開啟 AVI 檔案
ms.assetid: 322eb45f-7dd3-40f4-b6bf-381021c50397
keywords:
- AVIFileInit 函式
- AVIFileOpen 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7e8415e6cb3f54dc4eb6bffa11d7f70879546ff2a434fc75cbb91d283bb65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373257"
---
# <a name="opening-an-avi-file"></a>開啟 AVI 檔案

下列範例會使用 [**AVIFileInit**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) 函式來初始化 AVIFile 程式庫，並使用 [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) 函數來開啟 AVI 檔案。 函數會使用預設的檔案處理常式。


```C++
// LoadAVIFile - loads AVIFile and opens an AVI file. 
// 
// szfile - filename 
// hwnd - window handle 
// 
VOID LoadAVIFile(LPCSTR szFile, HWND hwnd) 
{ 
    LONG hr; 
    PAVIFILE pfile; 
 
    AVIFileInit();          // opens AVIFile library 
 
    hr = AVIFileOpen(&pfile, szFile, OF_SHARE_DENY_WRITE, 0L); 
    if (hr != 0){ 
        // Handle failure.
        return; 
    } 
 
// 
// Place functions here that interact with the open file. 
// 
 
    AVIFileRelease(pfile);  // closes the file 
    AVIFileExit();          // releases AVIFile library 
} 
 
```



 

 




