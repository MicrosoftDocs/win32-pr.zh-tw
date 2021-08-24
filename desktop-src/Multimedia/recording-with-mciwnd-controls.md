---
title: 使用 MCIWnd 控制項錄製
description: 使用 MCIWnd 控制項錄製
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- MCIWndCreate 函式
- MCIWndNew 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a02dfd62985b0267c685e6893512f977340f47f95801e8821d46005d5371397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805558"
---
# <a name="recording-with-mciwnd-controls"></a>使用 MCIWnd 控制項錄製

下列範例會使用 MCIWnd 視窗的內建控制項來記錄波形音訊。 此範例會使用 MCIWNDF \_ 記錄視窗樣式和 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式來建立 MCIWnd 視窗，以將 [ **記錄** ] 按鈕加入工具列。 [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)宏指出與 MCIWnd 視窗相關聯的新檔案，而波形音訊裝置將提供其內容。 第二個功能表命令 IDM \_ SAVEMCIWND，可讓使用者儲存錄製，並使用 [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) 宏來選取檔案名。


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




