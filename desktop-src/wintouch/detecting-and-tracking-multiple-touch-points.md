---
title: 偵測和追蹤多個觸控點
description: 偵測和追蹤多個觸控點
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows觸控、多個觸控點
- 偵測多個觸控點
- 追蹤多個觸控點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5b8086988dc1a87b5596d5a0ac74ec1f1df5ce4b85d928cbe306b791d17b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118436042"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a>偵測和追蹤多個觸控點

下列步驟說明如何使用 Windows Touch 來追蹤多個觸控點。

1.  建立應用程式並啟用 Windows Touch。
2.  為 [**WM \_ 觸控**](wm-touchdown.md) 和追蹤點新增處理常式。
3.  繪製點。

當您的應用程式執行之後，它會在每個觸控下呈現圓形。 下列螢幕擷取畫面會顯示您的應用程式在執行時的外觀。

![顯示將觸控點轉譯為綠色和黃色圓形的應用程式螢幕擷取畫面](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a>建立應用程式並啟用 Windows Touch

使用 Microsoft Visual Studio wizard，從 Microsoft Win32 應用程式開始。 完成嚮導之後，請在 targetver.h 中設定 Windows 版本，並在您的應用程式中包含 Windows .h 和 windowsx，以新增 Windows Touch 訊息的支援。 下列程式碼顯示如何在 targetver.h 中設定 Windows 版本。


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows 7.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows 7.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif     

#ifndef _WIN32_WINDOWS          // Specifies that the minimum required platform is Windows 98.
#define _WIN32_WINDOWS 0x0410 // Change this to the appropriate value to target Windows Me or later.
#endif

#ifndef _WIN32_IE                       // Specifies that the minimum required platform is Internet Explorer 7.0.
#define _WIN32_IE 0x0700        // Change this to the appropriate value to target other versions of IE.
#endif
```



下列程式碼顯示如何加入 include 指示詞。 此外，您可以建立一些稍後將使用的全域變數。


```C++
#include <windows.h>    // included for Windows Touch
#include <windowsx.h>   // included for point conversion

#define MAXPOINTS 10

// You will use this array to track touch points
int points[MAXPOINTS][2];

// You will use this array to switch the color / track ids
int idLookup[MAXPOINTS];


// You can make the touch points larger
// by changing this radius value
static int radius      = 50;

// There should be at least as many colors
// as there can be touch points so that you
// can have different colors for each point
COLORREF colors[] = { RGB(153,255,51), 
                      RGB(153,0,0), 
                      RGB(0,153,0), 
                      RGB(255,255,0), 
                      RGB(255,51,204), 
                      RGB(0,0,0),
                      RGB(0,153,0), 
                      RGB(153, 255, 255), 
                      RGB(153,153,255), 
                      RGB(0,51,153)
                    };

```



## <a name="add-handler-for-wm_touch-and-track-points"></a>為 WM \_ 觸控和追蹤點新增處理常式

首先，宣告 [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))中的 [**WM \_ 觸控**](wm-touchdown.md)處理常式所使用的一些變數。


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



現在，初始化用來儲存觸控點的變數，並從 **InitInstance** 方法註冊觸控輸入的視窗。


```C++
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd) {
      return FALSE;
   }

   // register the window for touch instead of gestures
   RegisterTouchWindow(hWnd, 0);  

   // the following code initializes the points
   for (int i=0; i< MAXPOINTS; i++){
     points[i][0] = -1;
     points[i][1] = -1;
     idLookup[i]  = -1;
   }  

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



接下來，從 [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))方法處理 [**WM \_ 觸控**](wm-touchdown.md)訊息。 下列程式碼顯示適用于 **WM \_ 觸控** 的處理常式的執行。


```C++
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
```



> [!Note]  
> 若要使用 [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) 函式，您的應用程式中必須有高 DPI 支援。 如需有關支援高 DPI 的詳細資訊，請參閱 MSDN 的 [高 DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) 區段。

 

現在當使用者接觸螢幕時，他或她所觸及的位置將會儲存在點陣列中。 [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput)結構的 **dwID** 成員會儲存與硬體相依的識別碼。

為了解決 dwID 成員相依于硬體的問題， [**WM \_ 觸控**](wm-touchdown.md)案例處理常式會使用 **GetContactIndex** 的函式，將 [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput)結構的 **dwID** 成員對應至在螢幕上繪製的點。 下列程式碼顯示此函式的實作為。


```C++
// This function is used to return an index given an ID
int GetContactIndex(int dwID){
  for (int i=0; i < MAXPOINTS; i++){
    if (idLookup[i] == -1){
      idLookup[i] = dwID;
      return i;
    }else{
      if (idLookup[i] == dwID){
        return i;
      }
    }
  }
  // Out of contacts
  return -1;
}
```



## <a name="draw-the-points"></a>繪製點

為繪圖常式宣告下列變數。


```C++
    // For double buffering
    static HDC memDC       = 0;
    static HBITMAP hMemBmp = 0;
    HBITMAP hOldBmp        = 0;
   
    // For drawing / fills
    PAINTSTRUCT ps;
    HDC hdc;
    
    // For tracking dwId to points
    int index;
```



記憶體顯示內容 *memDC* 是用來儲存暫存圖形內容，此內容會與轉譯的顯示內容（ *hdc*）交換以消除閃爍。 執行繪圖常式，以取得您所儲存的點，並在點繪製圓形。 下列程式碼顯示如何執行 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 處理常式。


```C++
  case WM_PAINT:
    hdc = BeginPaint(hWnd, &ps);    
    RECT client;
    GetClientRect(hWnd, &client);        
  
    // start double buffering
    if (!memDC){
      memDC = CreateCompatibleDC(hdc);
    }
    hMemBmp = CreateCompatibleBitmap(hdc, client.right, client.bottom);
    hOldBmp = (HBITMAP)SelectObject(memDC, hMemBmp);          
  
    FillRect(memDC, &client, CreateSolidBrush(RGB(255,255,255)));
     
    //Draw Touched Points                
    for (i=0; i < MAXPOINTS; i++){        
      SelectObject( memDC, CreateSolidBrush(colors[i]));           
      x = points[i][0];
      y = points[i][1];
      if  (x >0 && y>0){              
        Ellipse(memDC, x - radius, y - radius, x+ radius, y + radius);
      }
    }
  
    BitBlt(hdc, 0,0, client.right, client.bottom, memDC, 0,0, SRCCOPY);      

    EndPaint(hWnd, &ps);
    break;
```



當您執行應用程式時，它現在應該看起來像是本節開頭的圖例。

有趣的是，您可以在觸控點周圍繪製一些額外的線。 下列螢幕擷取畫面顯示應用程式如何查看在圓形周圍繪製的一些額外的線。

![顯示應用程式的螢幕擷取畫面，可將觸控點轉譯為具有直線的圓形，並與觸控點的邊緣相交](images/multitouchpointsfun.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows觸控輸入](guide-multi-touch-input.md)
</dt> </dl>

 

 