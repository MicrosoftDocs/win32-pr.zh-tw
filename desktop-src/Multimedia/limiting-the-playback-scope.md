---
title: 限制播放範圍
description: 限制播放範圍
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- MCIWndPlayFrom 宏
- MCIWndPlayTo 宏
- MCIWndPlayFromTo 宏
- MCI 播放命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839759"
---
# <a name="limiting-the-playback-scope"></a>限制播放範圍

控制播放的開頭是 [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 宏，它會將與 MCIWnd 視窗相關聯的內容或檔案從目前的播放位置播放到內容結尾。 如果您想要將播放限制在內容或檔案的特定部分，您可以從其他播放 MCIWnd 宏選擇： [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom)、 [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)和 [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto)。

您也需要設定適當的時間格式。 時間格式會決定內容是以框架、毫秒、曲目或某些其他單位來測量。

下列範例會建立一個 MCIWnd 視窗，並提供功能表命令來播放最後三個、第三個或第三個內容。 這些功能表命令會使用 **MCIWndPlayFrom**、 **MCIWndPlayTo** 和 **MCIWndPlayFromTo** 來播放內容區段。 此範例也會使用 [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) 和 [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) 宏來識別內容的開頭和結尾，並使用 [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) 宏將播放位置移至內容的開頭。

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)函式 \_ 除了標準視窗樣式之外，還會使用 WS 標題和 MCIWNDF \_ SHOWALL 樣式，以在 MCIWnd 視窗的標題列中顯示檔案名、模式和目前的播放位置。


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




