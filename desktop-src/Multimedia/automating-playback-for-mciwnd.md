---
title: 自動播放 MCIWnd
description: 自動播放 MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- MCIWndCreate 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b9224cfa4f5a93488f226d1aefa83201b8b0637
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311132"
---
# <a name="automating-playback-for-mciwnd"></a>自動播放 MCIWnd

您可以在 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式中指定特定的視窗樣式，以自動化 MCIWnd 的播放。 若要播放裝置，視窗需要父視窗來處理通知訊息、播放 AVI 檔案的播放區域，以及裝置模式變更的通知，以識別播放何時停止。 視窗不需要工具列。 您可以藉由在 **MCIWndCreate** 中指定適當的樣式來設定這些特性。

下列範例會使用功能表命令來建立 MCIWnd 視窗，以從數個不同類型的裝置播放內容。 **MCIWndCreate** 函式會建立 MCIWnd 視窗，並使用裝置特定命令中的 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)宏載入裝置和檔案。 當裝置完成播放時，您會藉由捕捉 [**MCIWNDM \_ NOTIFYMODE**](mciwndm-notifymode.md) 訊息併發出 [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) 宏來關閉裝置。


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            dwMCIWndStyle = WS_CHILD |     // child window
                WS_VISIBLE |               // visible
                MCIWNDF_NOTIFYMODE |       // notifies of mode changes
                MCIWNDF_NOPLAYBAR;            // hides toolbar 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, dwMCIWndStyle, NULL); 
            break; 
        case IDM_PLAYCDA: 
            LoadNGoMCIWnd(hwnd, "CDAudio"); 
            break; 
        case IDM_PLAYWAVE: 
            LoadNGoMCIWnd(hwnd, "SoundWave.WAV"); 
            break; 
        case IDM_PLAYMIDI: 
            LoadNGoMCIWnd(hwnd, "MIDIFile.MID"); 
            break; 
        case IDM_PLAYAVI: 
            LoadNGoMCIWnd(hwnd, "AVIFile.AVI"); 
            break; 
        case IDM_EXIT: 
            MCIWndDestroy(g_hwndMCIWnd); 
            DestroyWindow(hwnd); 
            break; 
    } 
    break; 
 
case MCIWNDM_NOTIFYMODE: 
    if (lParam == MCI_MODE_STOP)  // device stopped
    { 
        MessageBox(hwnd,"","Closing Device",MB_OK); 
        MCIWndClose(g_hwndMCIWnd); 
    } 
    break; 

// Handle other messages here. 
 
// LoadNGoMCIWnd - automatically loads and plays a multimedia device 
// 
// hwnd -  handle to the parent window 
// lpstr - pointer to device or filename played by device 
// 
// Global variable 
// extern HINSTANCE g_hwndMCIWnd;  instance handle to MCIWnd window 
 
VOID LoadNGoMCIWnd(HWND hwnd, LPSTR lpstr) 
{ 
    MessageBox(hwnd, lpstr, "Loading Device", MB_OK); 
    MCIWndOpen(g_hwndMCIWnd, lpstr, NULL);   // new device in window 
    MCIWndPlay(g_hwndMCIWnd);                // plays device 
} 
```



 

 




