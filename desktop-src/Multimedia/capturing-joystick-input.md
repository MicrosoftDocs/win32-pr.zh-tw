---
title: 捕獲搖桿輸入
description: 捕獲搖桿輸入
ms.assetid: 1214fe5a-5a6a-4c6c-9b77-94eeb73f60da
keywords:
- 操縱杆，捕捉輸入
- 捕獲搖桿輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23fd3717ad09fd2e52f1a815f7d13b91963a13e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092717"
---
# <a name="capturing-joystick-input"></a>捕獲搖桿輸入

控制搖桿的大部分程式碼都是在主視窗函式中。 在訊息處理常式的下列部分中，應用程式會呼叫 [**joySetCapture**](/windows/win32/api/joystickapi/nf-joystickapi-joysetcapture) 來從搖桿 JOYSTICKID1 抓取輸入。


```C++
case WM_CREATE: 
    if(joySetCapture(hWnd, JOYSTICKID1, NULL, FALSE)) 
    { 
        MessageBeep(MB_ICONEXCLAMATION); 
        MessageBox(hWnd, "Couldn't capture the joystick.", NULL, 
            MB_OK | MB_ICONEXCLAMATION); 
        PostMessage(hWnd,WM_CLOSE,0,0L); 
    } 
    break; 
 
```



 

 