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
ms.openlocfilehash: 1c8c3421b3d7f59e7f6b16150fcd0d641deaef17
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300516"
---
# <a name="installing-compressors-and-decompressors"></a><span data-ttu-id="632ae-106">安裝壓縮機和 Decompressors</span><span class="sxs-lookup"><span data-stu-id="632ae-106">Installing Compressors and Decompressors</span></span>

<span data-ttu-id="632ae-107">下列範例顯示應用程式如何使用 [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) 函式，將函式安裝為壓縮程式或解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="632ae-107">The following example shows how an application can install a function as a compressor or decompressor using the [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall) function.</span></span>


```C++
// This function looks like a DriverProc entry point. 

LRESULT MyCodecFunction(DWORD dwID, HDRVR hDriver, 
    UINT uiMessage, LPARAM lParam1, LPARAM lParam2); 
 
// This function installs the MyCodecFunction as a compressor. 

result = ICInstall ( ICTYPE_VIDEO, mmioFOURCC('s','a','m','p'), 
    (LPARAM)(FARPROC)&MyCodecFunction, NULL, ICINSTALL_FUNCTION); 
 
```



 

 




