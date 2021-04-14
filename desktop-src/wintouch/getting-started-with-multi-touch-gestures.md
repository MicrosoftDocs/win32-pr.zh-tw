---
title: 使用 Windows Touch 手勢開始使用
description: 本節說明使用多點觸控手勢的基本步驟。
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows Touch，手勢
- Windows Touch，訊息
- 手勢，關於
- 手勢，訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371893"
---
# <a name="getting-started-with-windows-touch-gestures"></a>使用 Windows Touch 手勢開始使用

本節說明使用多點觸控手勢的基本步驟。

使用 Windows Touch 手勢時，通常會執行下列步驟：

1.  設定用來接收手勢的視窗。
2.  處理筆勢訊息。
3.  解讀手勢訊息。

## <a name="setting-up-a-window-to-receive-gestures"></a>設定視窗以接收手勢

根據預設，您會收到 [**WM \_ 手勢**](wm-gesture.md) 訊息。

> [!Note]  
> 如果您呼叫 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)，就會停止接收 [**WM \_ 手勢**](wm-gesture.md) 訊息。 如果您未收到 **WM \_ 手勢** 訊息，請確定您未呼叫 **RegisterTouchWindow**。

 

下列程式碼顯示簡單的 InitInstance 執行。


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a>處理手勢訊息

類似于處理 Windows Touch 輸入訊息，您可以透過許多方式來處理筆勢訊息。 如果您使用的是 Win32，則可以在 WndProc 中檢查 [**WM \_ 手勢**](wm-gesture.md) 訊息。 如果您要建立另一種類型的應用程式，您可以將 **WM \_ 手勢** 訊息新增至訊息對應，然後執行自訂處理常式。

下列程式碼顯示如何處理手勢訊息。


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a>解讀手勢訊息

[**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo)函式可用來將手勢訊息轉譯成描述手勢的結構。 結構 [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo)包含筆勢的相關資訊，例如執行筆勢的位置，以及筆勢的類型。 下列程式碼顯示如何取出和解讀手勢訊息。


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Touch 手勢](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




