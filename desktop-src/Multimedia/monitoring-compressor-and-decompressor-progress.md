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
ms.openlocfilehash: 724d3e6a8bee645717ef624eddd1276d3e55e856f1aab3c6edc5f9585b3f5feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137179"
---
# <a name="monitoring-compressor-and-decompressor-progress"></a>監視壓縮和解壓縮進程進度

下列範例示範如何使用 [**ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) 函式來通知壓縮程式或解壓縮回呼函數位址：


```C++
ICSetStatusProc(compvars.hic, 0, (LPARAM) (UINT) hwndApp, 
    &PreviewStatusProc); 
 
```



下列範例顯示前一個片段所安裝的回呼函數：


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



 

 




