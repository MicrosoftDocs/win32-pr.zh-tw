---
title: 自訂錄製流程
description: 自訂錄製流程
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- MCIWndCreate 函式
- MCIWndNew 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec46f61ef4624ba613025f01b081ccc1ebda1cad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932188"
---
# <a name="customizing-the-recording-process"></a>自訂錄製流程

您可以自訂錄製程式，完全掌控大部分的一切，從建立 MCIWnd 視窗到將記錄的資訊儲存在檔案中。 下列範例會查詢 MCI 裝置以進行錄製和儲存功能，並包含在內容開頭或結尾錄製的功能表命令。

下列範例會使用 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式來建立新的視窗，並可讓您指定現有的檔案來儲存記錄的資料，並使用 [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) 宏來建立新檔案與視窗之間的關聯。 或者，您可以使用 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) 或 [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) 宏來指定檔案。

此範例會使用 [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) 宏來確認裝置是否可以錄製，以及 [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) 宏來確認裝置是否儲存資訊。 此範例會使用 [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) 和 [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) 宏來設定目前的播放位置。 此範例會使用 [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) 宏來開始錄製。 記錄資訊之後，範例會使用 [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) 宏儲存它。


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, g_hinst, 
                WS_VISIBLE | WS_CHILD | 
                MCIWNDF_RECORD,                   // add Record button
                NULL ); 
 
            MCIWndNew(g_hwndMCIWnd, "waveaudio"); // new file 
 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MessageBox( hwnd, 
                "Press the red button on the toolbar to record.", 
                "MCIWnd Record", 
                MB_OK ); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK ); 
            } 
            break; 
        case IDM_RECORDATSTART: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndHome(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_RECORDATEND: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndEnd(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_SAVEMCIWND: 
            if( MCIWndCanSave(g_hwndMCIWnd) ) 
                MCIWndSaveDialog(g_hwndMCIWnd); 
    } 
    break; 
 
    // Handle other messages here. 
```



 

 




