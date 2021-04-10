---
title: 處理操縱杆訊息
description: 處理操縱杆訊息
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- 操縱杆，訊息
- MM_JOY1MOVE 訊息
- MM_JOY1BUTTONDOWN 訊息
- MM_JOY1BUTTONUP 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021250"
---
# <a name="processing-joystick-messages"></a><span data-ttu-id="4ec55-107">處理操縱杆訊息</span><span class="sxs-lookup"><span data-stu-id="4ec55-107">Processing Joystick Messages</span></span>

<span data-ttu-id="4ec55-108">下列範例說明應用程式如何回應搖桿的移動以及按鈕狀態的變更。</span><span class="sxs-lookup"><span data-stu-id="4ec55-108">The following example illustrates how an application could respond to joystick movements and changes in the button states.</span></span> <span data-ttu-id="4ec55-109">當搖桿變更位置時，應用程式會移動游標，並在按下任一按鈕時，在桌面上繪製專案符號孔。</span><span class="sxs-lookup"><span data-stu-id="4ec55-109">When the joystick changes position, the application moves the cursor and, if either button is pressed, draws a bullet hole on the desktop.</span></span> <span data-ttu-id="4ec55-110">當您按下游戲杆按鈕時，應用程式會在桌上型電腦上繪製一個洞，並持續播放音效直到按鈕放開為止。</span><span class="sxs-lookup"><span data-stu-id="4ec55-110">When a joystick button is pressed, the application draws a hole on the desktop and plays a sound continuously until a button is released.</span></span> <span data-ttu-id="4ec55-111">要監看的訊息為 [**mm \_ JOY1MOVE**](mm-joy1move.md)、 [**mm \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md)和 [**mm \_ JOY1BUTTONUP**](mm-joy1buttonup.md)。</span><span class="sxs-lookup"><span data-stu-id="4ec55-111">The messages to watch are [**MM\_JOY1MOVE**](mm-joy1move.md), [**MM\_JOY1BUTTONDOWN**](mm-joy1buttondown.md), and [**MM\_JOY1BUTTONUP**](mm-joy1buttonup.md).</span></span>


```C++
case MM_JOY1MOVE :                     // changed position 
    if((UINT) wParam & (JOY_BUTTON1 | JOY_BUTTON2)) 
        DrawFire(hWnd); 
    DrawSight(lParam);                 // calculates new cursor position 
    break; 
case MM_JOY1BUTTONDOWN :               // button is down 
    if((UINT) wParam & JOY_BUTTON1) 
    { 
        PlaySound(lpButton1, SND_LOOP | SND_ASYNC | SND_MEMORY); 
        DrawFire(hWnd); 
    } 
    else if((UINT) wParam & JOY_BUTTON2) 
    { 
        PlaySound(lpButton2, SND_ASYNC | SND_MEMORY |  SND_LOOP); 
        DrawFire(hWnd); 
    } 
    break; 
case MM_JOY1BUTTONUP :                 // button is up 
    sndPlaySound(NULL, 0);             // stops the sound 
    break; 

```



 

 




