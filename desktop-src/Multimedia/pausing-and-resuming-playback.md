---
title: 暫停和繼續播放
description: 暫停和繼續播放
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- MCIWndPause 宏
- MCIWndResume 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1876417b821a57f7ebbac0cd35bec184cc9d2da
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932104"
---
# <a name="pausing-and-resuming-playback"></a><span data-ttu-id="32a09-105">暫停和繼續播放</span><span class="sxs-lookup"><span data-stu-id="32a09-105">Pausing and Resuming Playback</span></span>

<span data-ttu-id="32a09-106">您可以使用 [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) 宏，中斷與 MCIWnd 視窗相關聯的裝置或檔案的播放。</span><span class="sxs-lookup"><span data-stu-id="32a09-106">You can interrupt playback of a device or file associated with an MCIWnd window by using the [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) macro.</span></span> <span data-ttu-id="32a09-107">然後，您可以使用 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 宏重新開機播放。</span><span class="sxs-lookup"><span data-stu-id="32a09-107">You can then restart playback by using the [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) macro.</span></span> <span data-ttu-id="32a09-108">如果裝置不支援 resume 或發生錯誤，您可以使用 [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) 宏重新開機播放。</span><span class="sxs-lookup"><span data-stu-id="32a09-108">If the device does not support resume or if an error occurs, you can use the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro to restart playback.</span></span>

<span data-ttu-id="32a09-109">下列範例會建立 MCIWnd 視窗並播放 AVI 檔。</span><span class="sxs-lookup"><span data-stu-id="32a09-109">The following example creates an MCIWnd window and plays an AVI file.</span></span> <span data-ttu-id="32a09-110">使用者可以使用 [暫停] 和 [繼續] 功能表命令來中斷並重新啟動播放。</span><span class="sxs-lookup"><span data-stu-id="32a09-110">Pause and resume menu commands are available to the user to interrupt and restart playback.</span></span>

<span data-ttu-id="32a09-111">MCIWnd 視窗樣式會暫時變更，方法是使用 [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) 宏來防止在 [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) 失敗時顯示 MCI 錯誤對話方塊。</span><span class="sxs-lookup"><span data-stu-id="32a09-111">MCIWnd window styles are changed temporarily by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to inhibit an MCI error dialog box from being displayed if [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) fails.</span></span>


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



 

 




