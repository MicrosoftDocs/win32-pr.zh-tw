---
title: 監視壓縮和解壓縮進程進度
description: 監視壓縮和解壓縮進程進度
ms.assetid: 7c87c688-75b6-4d3e-9dd5-5f509ff2e473
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，監視
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，監視
- ICSetStatusProc 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb86a40bb653380dc93e758ada1b2eef6ec9ca7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021327"
---
# <a name="monitoring-compressor-and-decompressor-progress"></a><span data-ttu-id="9f098-106">監視壓縮和解壓縮進程進度</span><span class="sxs-lookup"><span data-stu-id="9f098-106">Monitoring Compressor and Decompressor Progress</span></span>

<span data-ttu-id="9f098-107">下列範例示範如何使用 [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) 函式來通知壓縮程式或解壓縮回呼函數位址：</span><span class="sxs-lookup"><span data-stu-id="9f098-107">The following example shows how the [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) function is used to inform the compressor or decompressor of the callback function address:</span></span>


```C++
ICSetStatusProc(compvars.hic, 0, (LPARAM) (UINT) hwndApp, 
    &PreviewStatusProc); 
 
```



<span data-ttu-id="9f098-108">下列範例顯示前一個片段所安裝的回呼函數：</span><span class="sxs-lookup"><span data-stu-id="9f098-108">The following example shows the callback function installed by the previous fragment:</span></span>


```C++
LONG CALLBACK export PreviewStatusProc(LPARAM lParam, 
    UINT message, LONG l) 
{ 
    switch (message) 
    { 
        MSG msg; 
        case ICSTATUS_START: 
         
        // Create and display status dialog box. 
         
            break; 
        case ICSTATUS_STATUS: 
            ProSetBarPos((int) l); // sets status bar positions 
 
        // Watch for abort message 
            while(PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                if (msg.message == WM_KEYDOWN && msg.wParam == 
                    VK_ESCAPE) 
                    return 1; 
                if (msg.message == WM_SYSCOMMAND && 
                    (msg.wParam & 0xFFF0) == SC_CLOSE) 
                    return 1; 
 
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
            break; 
        case ICSTATUS_END: 
         
        // Close and destroy status dialog box. 
         
            break; 
        case ICSTATUS_YIELD: 
         
         
         
            break; 
    } 
    return 0; 
} 
 
```



 

 




