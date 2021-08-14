---
description: 若要回應 WM \_ 油漆訊息，請使用如下所示的程式碼。
ms.assetid: 682d9bc6-8d74-48c4-80fb-bae73d409a6b
title: 在橫跨多個顯示器的 DC 上繪製
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550279d003c7d32fc97923ea6ebe4c95364773e514a69e4c66bdb4b100784384
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118759479"
---
# <a name="painting-on-a-dc-that-spans-multiple-displays"></a>在橫跨多個顯示器的 DC 上繪製

若要回應 **WM \_ 油漆** 訊息，請使用如下所示的程式碼。


```C++
case WM_PAINT:
hdc = BeginPaint(hwnd, &ps);
EnumDisplayMonitors(hdc, NULL, MyPaintEnumProc, 0);
EndPaint(hwnd, &ps);
 
```



若要繪製視窗的上半部，請使用如下所示的程式碼。


```C++
GetClient Rect(hwnd, &rc);
rc.bottom = (rc.bottom - rc.top) / 2;
hdc = GetDC(hwnd);
EnumDisplayMonitors(hdc, &rc, MyPaintEnumProc, 0);
ReleaseDC(hwnd, hdc);
```



若要以最佳方式繪製每個監視器的整個虛擬畫面，請使用如下所示的程式碼。


```C++
hdc = GetDC(NULL);
EnumDisplayMonitors(hdc, NULL, MyPaintScreenEnumProc, 0);
ReleaseDC(NULL, hdc);
```



 

 



