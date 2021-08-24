---
title: 暫停和繼續播放
description: 暫停和繼續播放
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- MCIWndPause 宏
- MCIWndResume 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce70a95000cda6fc471967e5075b16fe7bad837c71eed4e6216ddeaddddc4508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805968"
---
# <a name="pausing-and-resuming-playback"></a>暫停和繼續播放

您可以使用 [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) 宏，中斷與 MCIWnd 視窗相關聯的裝置或檔案的播放。 然後，您可以使用 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 宏重新開機播放。 如果裝置不支援 resume 或發生錯誤，您可以使用 [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 宏重新開機播放。

下列範例會建立 MCIWnd 視窗並播放 AVI 檔。 使用者可以使用 [暫停] 和 [繼續] 功能表命令來中斷並重新啟動播放。

MCIWnd 視窗樣式會暫時變更，方法是使用 [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) 宏來防止在 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 失敗時顯示 MCI 錯誤對話方塊。


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND:             // creates and plays clip 
            g_hwndMCIWnd = MCIWndCreate(hwnd,  
                g_hinst,                      
                WS_CHILD | WS_VISIBLE |    // standard styles
                MCIWNDF_NOPLAYBAR |        // hides toolbar 
                MCIWNDF_NOTIFYMODE,        // notifies of mode changes
                "sample.avi"); 
 
            MCIWndPlay(g_hwndMCIWnd); 
            break;    
        case IDM_PAUSEMCIWND:              // pauses playback 
            MCIWndPause(g_hwndMCIWnd); 
            MessageBox(hwnd, "MCIWnd", "Pausing Playback", MB_OK); 
            break; 
        case IDM_RESUMEMCIWND:          // resumes playback 
            MCIWndChangeStyles(      // hides error dialog messages
                g_hwndMCIWnd,        // MCIWnd window
                MCIWNDF_NOERRORDLG,  // mask of style to change
                MCIWNDF_NOERRORDLG); // suppresses MCI error dialogs 
 
            lResult = MCIWndResume(g_hwndMCIWnd); 
 
            if(lResult){                   // device doesn't resume 
                MessageBox(hwnd, "MCIWnd", 
                    "Resume with Stop and Play", MB_OK); 
                MCIWndStop(g_hwndMCIWnd); 
                MCIWndPlay(g_hwndMCIWnd); 
 
                MCIWndChangeStyles(        // resumes original styles
                    g_hwndMCIWnd, 
                    MCIWNDF_NOERRORDLG, 
                    NULL); 
        } 
        break; 
    } 
    break; 
 
// Handle other messages here. 
```



 

 




