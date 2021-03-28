---
description: 本主題將示範如何使用 GDI 加號繪製線條。
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: 繪製線條
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5284a178baab624633dd427cad84b35933a72fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972896"
---
# <a name="drawing-a-line"></a><span data-ttu-id="c3c43-103">繪製線條</span><span class="sxs-lookup"><span data-stu-id="c3c43-103">Drawing a Line</span></span>

<span data-ttu-id="c3c43-104">本主題將示範如何使用 GDI 加號繪製線條。</span><span class="sxs-lookup"><span data-stu-id="c3c43-104">This topic demonstrates how to draw a line using GDI Plus.</span></span>

<span data-ttu-id="c3c43-105">若要在 Windows GDI + 中繪製線條，您需要 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件、 [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 物件和 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 物件。</span><span class="sxs-lookup"><span data-stu-id="c3c43-105">To draw a line in Windows GDI+ you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="c3c43-106">**Graphics** 物件提供 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint))方法，而 **Pen** 物件會保存線條的屬性，例如色彩和寬度。</span><span class="sxs-lookup"><span data-stu-id="c3c43-106">The **Graphics** object provides the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method, and the **Pen** object holds attributes of the line, such as color and width.</span></span> <span data-ttu-id="c3c43-107">**畫筆** 物件的位址會做為引數傳遞至 **DrawLine** 方法。</span><span class="sxs-lookup"><span data-stu-id="c3c43-107">The address of the **Pen** object is passed as an argument to the **DrawLine** method.</span></span>

<span data-ttu-id="c3c43-108">下列程式會繪製從 (0，0) 到 (200，100) 的行，其中包含三個函數： **WinMain**、 **WndProc** 和 **OnPaint**。</span><span class="sxs-lookup"><span data-stu-id="c3c43-108">The following program, which draws a line from (0, 0) to (200, 100), consists of three functions: **WinMain**, **WndProc**, and **OnPaint**.</span></span> <span data-ttu-id="c3c43-109">**WinMain** 和 **WndProc** 函式提供大部分 Windows 應用程式通用的基本程式碼。</span><span class="sxs-lookup"><span data-stu-id="c3c43-109">The **WinMain** and **WndProc** functions provide the fundamental code common to most Windows applications.</span></span> <span data-ttu-id="c3c43-110">**WndProc** 函數中沒有任何 gdi + 程式碼。</span><span class="sxs-lookup"><span data-stu-id="c3c43-110">There is no GDI+ code in the **WndProc** function.</span></span> <span data-ttu-id="c3c43-111">**WinMain** 函式具有少量的 gdi + 程式碼，也就是 [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup)和 [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown)所需的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c3c43-111">The **WinMain** function has a small amount of GDI+ code, namely the required calls to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) and [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown).</span></span> <span data-ttu-id="c3c43-112">實際建立 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件並繪製線條的 gdi + 程式碼會在 **OnPaint** 函式中。</span><span class="sxs-lookup"><span data-stu-id="c3c43-112">The GDI+ code that actually creates a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and draws a line is in the **OnPaint** function.</span></span>

<span data-ttu-id="c3c43-113">**OnPaint** 函式會接收裝置內容的控制碼，並將該控制碼傳遞給 [**圖形**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)的函式。</span><span class="sxs-lookup"><span data-stu-id="c3c43-113">The **OnPaint** function receives a handle to a device context and passes that handle to a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) constructor.</span></span> <span data-ttu-id="c3c43-114">傳遞給 [**畫筆**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) 參數的引數是 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="c3c43-114">The argument passed to the [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) constructor is a reference to a [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) object.</span></span> <span data-ttu-id="c3c43-115">傳遞給 color 函式的四個數字代表色彩的 Alpha、紅色、綠色和藍色元件。</span><span class="sxs-lookup"><span data-stu-id="c3c43-115">The four numbers passed to the color constructor represent the alpha, red, green, and blue components of the color.</span></span> <span data-ttu-id="c3c43-116">Alpha 元件會決定色彩的透明度;0是完全透明的，而255則完全不透明。</span><span class="sxs-lookup"><span data-stu-id="c3c43-116">The alpha component determines the transparency of the color; 0 is fully transparent and 255 is fully opaque.</span></span> <span data-ttu-id="c3c43-117">傳遞至 [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) 方法的四個數字，代表起點 (0、0) 和結束點 (200，100) 。</span><span class="sxs-lookup"><span data-stu-id="c3c43-117">The four numbers passed to the [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) method represent the starting point (0, 0) and the ending point (200, 100) of the line.</span></span>


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



<span data-ttu-id="c3c43-118">請注意 **WinMain** 函數中對 [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="c3c43-118">Note the call to [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) in the **WinMain** function.</span></span> <span data-ttu-id="c3c43-119">**GdiplusStartup** 函數的第一個參數是 ULONG PTR 的位址 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3c43-119">The first parameter of the **GdiplusStartup** function is the address of a ULONG\_PTR.</span></span> <span data-ttu-id="c3c43-120">**GdiplusStartup** 會使用稍後傳遞給 [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) 函式的權杖來填滿該變數。</span><span class="sxs-lookup"><span data-stu-id="c3c43-120">**GdiplusStartup** fills that variable with a token that is later passed to the [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) function.</span></span> <span data-ttu-id="c3c43-121">**GdiplusStartup** 函數的第二個參數是 [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="c3c43-121">The second parameter of the **GdiplusStartup** function is the address of a [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) structure.</span></span> <span data-ttu-id="c3c43-122">上述程式碼依賴預設的 **GdiplusStartupInput** 函式來適當地設定結構成員。</span><span class="sxs-lookup"><span data-stu-id="c3c43-122">The preceding code relies on the default **GdiplusStartupInput** constructor to set the structure members appropriately.</span></span>

 

 



