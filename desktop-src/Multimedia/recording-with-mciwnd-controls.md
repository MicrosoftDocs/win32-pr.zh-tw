---
title: 使用 MCIWnd 控制項錄製
description: 使用 MCIWnd 控制項錄製
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- MCIWndCreate 函式
- MCIWndNew 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931927"
---
# <a name="recording-with-mciwnd-controls"></a><span data-ttu-id="3d71d-105">使用 MCIWnd 控制項錄製</span><span class="sxs-lookup"><span data-stu-id="3d71d-105">Recording with MCIWnd Controls</span></span>

<span data-ttu-id="3d71d-106">下列範例會使用 MCIWnd 視窗的內建控制項來記錄波形音訊。</span><span class="sxs-lookup"><span data-stu-id="3d71d-106">The following example records waveform audio using the built-in controls of the MCIWnd window.</span></span> <span data-ttu-id="3d71d-107">此範例會使用 MCIWNDF \_ 記錄視窗樣式和 [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) 函式來建立 MCIWnd 視窗，以將 [ **記錄** ] 按鈕加入工具列。</span><span class="sxs-lookup"><span data-stu-id="3d71d-107">The example creates an MCIWnd window by using the MCIWNDF\_RECORD window style with the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to add a **Record** button to the toolbar.</span></span> <span data-ttu-id="3d71d-108">[**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew)宏指出與 MCIWnd 視窗相關聯的新檔案，而波形音訊裝置將提供其內容。</span><span class="sxs-lookup"><span data-stu-id="3d71d-108">The [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro indicates a new file is associated with the MCIWnd window and that a waveform-audio device will provide its content.</span></span> <span data-ttu-id="3d71d-109">第二個功能表命令 IDM \_ SAVEMCIWND，可讓使用者儲存錄製，並使用 [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) 宏來選取檔案名。</span><span class="sxs-lookup"><span data-stu-id="3d71d-109">A second menu command, IDM\_SAVEMCIWND, lets the user save the recording and select a filename by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


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



 

 




