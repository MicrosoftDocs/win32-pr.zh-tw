---
title: 延展影像
description: 延展影像
ms.assetid: 7cfd91c3-0ebd-47eb-a33d-c81a66f820e5
keywords:
- MCIWndGetDest 宏
- MCIWndPutDest 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0296cd31988ba79aeab9221fb41b4fd150ffc09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301664"
---
# <a name="stretching-an-image"></a><span data-ttu-id="4f0e3-105">延展影像</span><span class="sxs-lookup"><span data-stu-id="4f0e3-105">Stretching an Image</span></span>

<span data-ttu-id="4f0e3-106">下列範例會伸展影片剪輯的影像。</span><span class="sxs-lookup"><span data-stu-id="4f0e3-106">The following example stretches the images of a video clip.</span></span> <span data-ttu-id="4f0e3-107">它會使用 [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) 宏來增加目的矩形的維度。</span><span class="sxs-lookup"><span data-stu-id="4f0e3-107">It increases the dimensions of the destination rectangle by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span> <span data-ttu-id="4f0e3-108">播放區域的大小會保持不變，因此結果會是扭曲的影像。</span><span class="sxs-lookup"><span data-stu-id="4f0e3-108">The size of the playback area remains unchanged, so the result is a distorted, magnified image.</span></span> <span data-ttu-id="4f0e3-109">這些範例會使用 **MCIWndPutDest** 函式來定位相對於播放區域的目的地矩形，以提供一種方式來查看延伸影像的不同部分。</span><span class="sxs-lookup"><span data-stu-id="4f0e3-109">The examples uses the **MCIWndPutDest** function to reposition the destination rectangle with respect to the playback area, providing a way to view different portions of the stretched image.</span></span>


```C++
extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
               g_hinst, 
               WS_CHILD | WS_VISIBLE, 
               "sample.avi"); 
           break; 
 
       case  IDM_STRETCHIMAGE:      // stretch destination RECT 3:2, 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new destination 
           break; 
       case IDM_MOVEDOWN:           // move toward bottom of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top -= 100;                    // new boundaries 
           rCurrent.bottom -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination
           break; 
       case IDM_MOVEUP:             // move toward top of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top += 100;                    // new boundaries 
           rCurrent.bottom += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case IDM_MOVELEFT:           // move toward left edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.right += 100;                  // new boundaries 
           rCurrent.left += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case  IDM_MOVERIGHT:         // move toward right edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rCurrent.right -= 100;                  // new boundaries 
           rCurrent.left -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 




