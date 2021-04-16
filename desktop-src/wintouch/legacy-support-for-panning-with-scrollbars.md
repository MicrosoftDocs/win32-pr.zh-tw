---
title: 舊版支援移動捲軸
description: 本節說明如何在以 Windows 為基礎的應用程式中使用捲軸來移動流覽。
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch，舊版支援
- 使用捲軸移動流覽
- Windows Touch，使用捲軸移動
- Windows Touch、捲軸
- 捲軸、移動流覽
- 捲軸，舊版支援
- Windows Touch，手勢
- 手勢，使用捲軸移動
- Windows Touch，筆觸
- 筆觸，使用捲軸移動
- 筆觸，停用
- Windows Touch，滑鼠滾輪訊息
- 滑鼠滾輪訊息
- Windows Touch，自訂移動
- 移動流覽、捲軸
- 移動流覽，舊版支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104558925"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a>舊版支援移動捲軸

本節說明如何在以 Windows 為基礎的應用程式中使用捲軸來移動流覽。

在 Windows 7 中，移動手勢會產生 WM \_ \* 捲軸訊息，以啟用移動的舊版支援。 因為您的應用程式可能不支援所有的 WM \_ \* 捲軸訊息，所以移動流覽可能無法正常運作。 本主題說明您必須採取的步驟，以確保應用程式中的舊版移動流覽體驗如使用者預期般運作。

## <a name="overview"></a>概觀

下列各節說明如何啟用舊版的移動體驗：

-   使用捲軸來建立應用程式。
-   停用筆觸。
-   自訂移動流覽體驗。

## <a name="create-an-application-with-scroll-bars"></a>建立具有捲軸的應用程式

使用 Microsoft Visual Studio wizard 啟動新的 Win32 專案。 請確定應用程式類型已設為 Windows 應用程式。 您不需要啟用 Active Template Library (ATL) 的支援。 下圖顯示您的專案在啟動後的樣子。

![顯示沒有捲軸之視窗的螢幕擷取畫面](images/gpd-1.png)

接下來，啟用影像上的捲軸。 變更 **InitInstance** 中的視窗建立程式碼，讓 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 函式呼叫建立具有捲軸的視窗。 下列程式碼示範如何執行這項操作。


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



變更視窗建立程式碼之後，您的應用程式將會有捲軸。 下圖顯示應用程式目前的外觀。

![顯示具有垂直捲動條但沒有文字之視窗的螢幕擷取畫面](images/gpd-2.png)

在您變更視窗建立程式碼之後，請在應用程式中加入捲軸物件，並在其中加入一些要滾動的文字。 將下列程式碼放在 **WndProc** 方法的頂端。


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



接下來，請執行應用程式邏輯來設定文字度量的文字計算。 下列程式碼應取代 **WndProc** 函式中的現有 **WM \_ 建立** 案例。


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



接下來，在調整視窗大小時，執行重新計算文字區塊的應用程式邏輯。 下列程式碼應該放入 **WndProc** 中的訊息參數。


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



接下來，執行垂直捲動條訊息的應用程式邏輯。 下列程式碼應該放入 **WndProc** 中的訊息參數。


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



接下來，更新程式碼以重新繪製視窗。 下列程式碼應取代 **WndProc** 中的預設 **WM \_ 油漆** 案例。


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



現在當您建立並執行您的應用程式時，它應該會有使用中的文字和垂直捲動條。 下圖顯示您的應用程式可能外觀。

![顯示具有垂直捲動條和文字之視窗的螢幕擷取畫面](images/gpd-3.png)

## <a name="disable-flicks"></a>停用筆觸

若要改善您應用程式中的移動流覽體驗，您應該關閉筆觸。 若要這樣做，請在 *hWnd* 值初始化時，設定視窗屬性。 用於筆觸的值會儲存在 tpcshrd 標頭中，也必須包含在內。 在您建立 *hWnd* 之後，下列程式碼應該放在 include 指示詞和 **InitInstance** 函式中。

> [!Note]  
> 這適用于需要立即針對觸控或觸控事件進行回應的應用程式，而不是測試時間或距離閾值。

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a>自訂移動流覽體驗

根據預設，您可能會想要使用 Windows 7 提供的不同移動流覽體驗。 若要改善移動流覽體驗，您必須加入 [**WM \_ 手勢**](wm-gesture.md) 訊息的處理常式。 如需詳細資訊，請參閱 [改善 Single-Finger 移動體驗](improving-the-single-finger-panning-experience.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Touch 手勢](guide-multi-touch-gestures.md)
</dt> </dl>

 

 