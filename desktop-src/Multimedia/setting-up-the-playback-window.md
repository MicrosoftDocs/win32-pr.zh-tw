---
title: 設定播放視窗
description: 設定播放視窗
ms.assetid: 4cf27099-e5e5-48f8-8d61-0a3d0e0d9499
keywords:
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d612c01f0800bc70b19e0b9d7d1b83eb5654371a75720ba85828d3ed9f08f3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805408"
---
# <a name="setting-up-the-playback-window"></a>設定播放視窗

下列範例會尋找播放 AVI 檔案所需的維度、建立對應至該大小的視窗，然後使用 MCIAVI 驅動程式在視窗中播放該檔案。 它使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式


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



 

 