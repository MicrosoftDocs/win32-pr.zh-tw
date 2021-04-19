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
# <a name="creating-an-mciwnd-window"></a>建立 MCIWnd 視窗

[**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea)函式會註冊並建立 MCIWnd 視窗。 視窗可以是父代、子系或快顯視窗。 下列範例會建立 MCIWnd 視窗作為子視窗，並讓使用者藉由提供對 [播放程式]、[ **播放**]、[ **停止**] 和 [ **功能表** ] 按鈕的存取權來控制播放。 此範例會指定父視窗的控制碼，並為視窗樣式指定 **Null** ，因此 \_ 會使用 ws 子系、WS \_ BORDER 和 ws 可見的預設視窗樣式 \_ 來建立 MCIWnd 視窗。


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
> 您也可以針對父視窗控制碼和視窗樣式指定 **Null** ，在此情況下，預設視窗樣式會是 WS 重迭 \_ 和 ws \_ 可見的。

 

 

 




