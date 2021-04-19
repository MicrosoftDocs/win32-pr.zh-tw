---
title: 設定播放視窗
description: 設定播放視窗
ms.assetid: 4cf27099-e5e5-48f8-8d61-0a3d0e0d9499
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ed74a133f112935f9ff2ad451e84e3819cee6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106969701"
---
# <a name="setting-up-the-playback-window"></a><span data-ttu-id="e5d61-104">設定播放視窗</span><span class="sxs-lookup"><span data-stu-id="e5d61-104">Setting Up the Playback Window</span></span>

<span data-ttu-id="e5d61-105">下列範例會尋找播放 AVI 檔案所需的維度、建立對應至該大小的視窗，然後使用 MCIAVI 驅動程式在視窗中播放該檔案。</span><span class="sxs-lookup"><span data-stu-id="e5d61-105">The following example finds the dimensions needed to play an AVI file, creates a window corresponding to that size, and plays the file in the window by using the MCIAVI driver.</span></span> <span data-ttu-id="e5d61-106">它使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式</span><span class="sxs-lookup"><span data-stu-id="e5d61-106">It uses the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function</span></span>


```C++
HWND hwnd; 
MCI_DGV_RECT_PARMS mciRect; 
 
// Get the movie dimensions with MCI_WHERE. 
 
mciSendCommand(wDeviceID, MCI_WHERE, MCI_DGV_WHERE_SOURCE, 
    (DWORD)(LPSTR)&mciRect); 
 
// Create the playback window. Make it bigger for the border. 
// Note that the right and bottom members of RECT structures in MCI 
// are unusual; rc.right is set to the rectangle's width, and 
// rc.bottom is set to the rectangle's height.

hwndMovie = CreateWindow("mywindow", "Playback", 
    WS_CHILD|WS_BORDER, 0,0, 
    mciRect.rc.right+(2*GetSystemMetric(SM_CXBORDER)),
    mciRect.rc.bottom+(2*GetSystemMetric(SM_CYBORDER)), 
    hwndParent, hInstApp, NULL); 
 
if (hwndMovie){ 
    // Window created OK; make it the playback window. 
 
    MCI_DGV_WINDOW_PARMS mciWindow; 
 
    mciWindow.hWnd = hwndMovie; 
    mciSendCommand(wDeviceID, MCI_WINDOW, MCI_DGV_WINDOW_HWND, 
        (DWORD)(LPSTR)&mciWindow); 
 
} 
```



 

 