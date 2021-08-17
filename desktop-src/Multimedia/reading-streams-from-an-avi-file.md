---
title: 從 AVI 檔案讀取資料流程
description: 從 AVI 檔案讀取資料流程
ms.assetid: fa17cac4-bc6f-48ef-8960-286386b43c82
keywords:
- AVIStreamInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d42c4682c1875fffbea079ab9ef55d954f15d3e9d49c2da1309504da68aa92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371513"
---
# <a name="reading-streams-from-an-avi-file"></a>從 AVI 檔案讀取資料流程

下列副程式會從 AVI 檔案取得資料流程資訊，並從 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa)函數所傳回的 [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa)結構判斷資料流程類型。


```C++
// StreamTypes - opens the streams in an AVI file and determines 
// stream types. 
// 
// Global variables 
// gcpavi - count of streams in an AVI file 
// gapavi[] = array of stream-interface pointers 
 
void StreamTypes(HWND hwnd) 
{ 
    AVISTREAMINFO     avis; 
    LONG    r, lHeight = 0; 
    WORD    w; 
    int     i; 
    RECT    rc; 
 
// Walk through all streams. 
    for (i = 0; i < gcpavi; i++) { 
        AVIStreamInfo(gapavi[i], &avis, sizeof(avis)); 
 
        if (avis.fccType == streamtypeVIDEO) { 
 
        // Place video-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeAUDIO) { 
 
        // Place audio-processing functions here. 
 
        } 
        else if (avis.fccType == streamtypeTEXT) { 
 
        // Place text-processing functions here. 
 
        } 
    } 
} 
 
```



 

 




