---
description: 本主題將示範如何使用 GDI 加號繪製線條。
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: 繪製線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e2a330f24cd0d1771458d02b264cdaa493835477b40c95d05ca4bf71c8a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036806"
---
# <a name="drawing-a-line"></a>繪製線條

本主題將示範如何使用 GDI 加號繪製線條。

若要在 Windows 中繪製線條 GDI+ 您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件、 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen)物件和 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color)物件。 **Graphics** 物件提供 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法，而 **Pen** 物件會保存線條的屬性，例如色彩和寬度。 **畫筆** 物件的位址會做為引數傳遞至 **DrawLine** 方法。

下列程式會繪製從 (0，0) 到 (200，100) 的行，其中包含三個函數： **WinMain**、 **WndProc** 和 **OnPaint**。 **WinMain** 和 **WndProc** 函式提供大多數 Windows 應用程式通用的基礎程式碼。 **WndProc** 函數中沒有 GDI+ 程式碼。 **WinMain** 函式具有少量的 GDI+ 程式碼，也就是 [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup)和 [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown)所需的呼叫。 實際建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件和繪製線條的 GDI+ 程式碼位於 **OnPaint** 函數中。

**OnPaint** 函式會接收裝置內容的控制碼，並將該控制碼傳遞給 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)的函式。 傳遞給 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 參數的引數是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 物件的參考。 傳遞給 color 函式的四個數字代表色彩的 Alpha、紅色、綠色和藍色元件。 Alpha 元件會決定色彩的透明度;0是完全透明的，而255則完全不透明。 傳遞至 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) 方法的四個數字，代表起點 (0、0) 和結束點 (200，100) 。


```C++
#include <stdafx.h>
#include <windows.h>
#include <objidl.h>
#include <gdiplus.h>
using namespace Gdiplus;
#pragma comment (lib,"Gdiplus.lib")

VOID OnPaint(HDC hdc)
{
   Graphics graphics(hdc);
   Pen      pen(Color(255, 0, 0, 255));
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE, PSTR, INT iCmdShow)
{
   HWND                hWnd;
   MSG                 msg;
   WNDCLASS            wndClass;
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR           gdiplusToken;
   
   // Initialize GDI+.
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   wndClass.style          = CS_HREDRAW | CS_VREDRAW;
   wndClass.lpfnWndProc    = WndProc;
   wndClass.cbClsExtra     = 0;
   wndClass.cbWndExtra     = 0;
   wndClass.hInstance      = hInstance;
   wndClass.hIcon          = LoadIcon(NULL, IDI_APPLICATION);
   wndClass.hCursor        = LoadCursor(NULL, IDC_ARROW);
   wndClass.hbrBackground  = (HBRUSH)GetStockObject(WHITE_BRUSH);
   wndClass.lpszMenuName   = NULL;
   wndClass.lpszClassName  = TEXT("GettingStarted");
   
   RegisterClass(&wndClass);
   
   hWnd = CreateWindow(
      TEXT("GettingStarted"),   // window class name
      TEXT("Getting Started"),  // window caption
      WS_OVERLAPPEDWINDOW,      // window style
      CW_USEDEFAULT,            // initial x position
      CW_USEDEFAULT,            // initial y position
      CW_USEDEFAULT,            // initial x size
      CW_USEDEFAULT,            // initial y size
      NULL,                     // parent window handle
      NULL,                     // window menu handle
      hInstance,                // program instance handle
      NULL);                    // creation parameters
      
   ShowWindow(hWnd, iCmdShow);
   UpdateWindow(hWnd);
   
   while(GetMessage(&msg, NULL, 0, 0))
   {
      TranslateMessage(&msg);
      DispatchMessage(&msg);
   }
   
   GdiplusShutdown(gdiplusToken);
   return msg.wParam;
}  // WinMain

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, 
   WPARAM wParam, LPARAM lParam)
{
   HDC          hdc;
   PAINTSTRUCT  ps;
   
   switch(message)
   {
   case WM_PAINT:
      hdc = BeginPaint(hWnd, &ps);
      OnPaint(hdc);
      EndPaint(hWnd, &ps);
      return 0;
   case WM_DESTROY:
      PostQuitMessage(0);
      return 0;
   default:
      return DefWindowProc(hWnd, message, wParam, lParam);
   }
} // WndProc
```



請注意 **WinMain** 函數中對 [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup)的呼叫。 **GdiplusStartup** 函數的第一個參數是 ULONG PTR 的位址 \_ 。 **GdiplusStartup** 會使用稍後傳遞給 [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) 函式的權杖來填滿該變數。 **GdiplusStartup** 函數的第二個參數是 [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput)結構的位址。 上述程式碼依賴預設的 **GdiplusStartupInput** 函式來適當地設定結構成員。

 

 



