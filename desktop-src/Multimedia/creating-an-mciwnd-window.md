---
title: 建立 MCIWnd 視窗
description: 建立 MCIWnd 視窗
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- MCIWnd 視窗，建立
- MCIWndCreate 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968833"
---
# <a name="creating-an-mciwnd-window"></a><span data-ttu-id="45f69-105">建立 MCIWnd 視窗</span><span class="sxs-lookup"><span data-stu-id="45f69-105">Creating an MCIWnd Window</span></span>

<span data-ttu-id="45f69-106">[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)函式會註冊並建立 MCIWnd 視窗。</span><span class="sxs-lookup"><span data-stu-id="45f69-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function registers and creates an MCIWnd window.</span></span> <span data-ttu-id="45f69-107">視窗可以是父代、子系或快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="45f69-107">The window can be a parent, child, or pop-up window.</span></span> <span data-ttu-id="45f69-108">下列範例會建立 MCIWnd 視窗作為子視窗，並讓使用者藉由提供對 [播放程式]、[ **播放**]、[ **停止**] 和 [ **功能表** ] 按鈕的存取權來控制播放。</span><span class="sxs-lookup"><span data-stu-id="45f69-108">The following example creates an MCIWnd window as a child window and lets the user control playback by providing access to the trackbar and the **Play**, **Stop**, and **Menu** buttons.</span></span> <span data-ttu-id="45f69-109">此範例會指定父視窗的控制碼，並為視窗樣式指定 **Null** ，因此 \_ 會使用 ws 子系、WS \_ BORDER 和 ws 可見的預設視窗樣式 \_ 來建立 MCIWnd 視窗。</span><span class="sxs-lookup"><span data-stu-id="45f69-109">The example specifies a handle of a parent window and specifies **NULL** for the window styles, so the default window styles of WS\_CHILD, WS\_BORDER, and WS\_VISIBLE are used to create the MCIWnd window.</span></span>


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> <span data-ttu-id="45f69-110">您也可以針對父視窗控制碼和視窗樣式指定 **Null** ，在此情況下，預設視窗樣式會是 WS 重迭 \_ 和 ws \_ 可見的。</span><span class="sxs-lookup"><span data-stu-id="45f69-110">You could also specify **NULL** for both the parent window handle and the window styles, in which case the default window styles would be WS\_OVERLAPPED and WS\_VISIBLE.</span></span>

 

 

 




