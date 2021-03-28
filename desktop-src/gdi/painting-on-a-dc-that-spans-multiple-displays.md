---
description: 若要回應 WM \_ 油漆訊息，請使用如下所示的程式碼。
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: 在橫跨多個顯示器的 DC 上繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5b1b85c8aab20b7ef2415c1d67188ecab7728c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512868"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a><span data-ttu-id="d0d5d-103">在橫跨多個顯示器的 DC 上繪製</span><span class="sxs-lookup"><span data-stu-id="d0d5d-103">Painting on a DC That Spans Multiple Displays</span></span>

<span data-ttu-id="d0d5d-104">若要回應 **WM \_ 油漆** 訊息，請使用如下所示的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d0d5d-104">To respond to a **WM\_PAINT** message, use code like the following.</span></span>


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



<span data-ttu-id="d0d5d-105">若要繪製視窗的上半部，請使用如下所示的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d0d5d-105">To paint the top half of a window, use code like the following.</span></span>


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



<span data-ttu-id="d0d5d-106">若要以最佳方式繪製每個監視器的整個虛擬畫面，請使用如下所示的程式碼。</span><span class="sxs-lookup"><span data-stu-id="d0d5d-106">To paint the entire virtual screen optimally for each monitor, use code like the following.</span></span>


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



