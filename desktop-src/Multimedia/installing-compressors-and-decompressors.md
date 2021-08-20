---
title: 安裝壓縮機和 Decompressors
description: 安裝壓縮機和 Decompressors
ms.assetid: 8bcca000-c4c7-47e7-a4c0-5d0d1750176f
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，安裝壓縮機
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，安裝壓縮機
- ICInstall 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27a9bacc946a17bf4d70260cb077a7e3f17fe85760837cc7086144297f1f86c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140534"
---
# <a name="installing-compressors-and-decompressors"></a>安裝壓縮機和 Decompressors

下列範例顯示應用程式如何使用 [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) 函式，將函式安裝為壓縮程式或解壓縮程式。


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




