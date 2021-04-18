---
title: 偵測和追蹤多個觸控點
description: 偵測和追蹤多個觸控點
ms.assetid: 7a5c7595-f341-4e11-805f-ed0b9c63cbff
keywords:
- Windows Touch，多個觸控點
- 偵測多個觸控點
- 追蹤多個觸控點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13b9eaf665b850eea8925bd531ffd1e9ec3fcf40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463476"
---
# <a name="detecting-and-tracking-multiple-touch-points"></a><span data-ttu-id="5ec68-106">偵測和追蹤多個觸控點</span><span class="sxs-lookup"><span data-stu-id="5ec68-106">Detecting and Tracking Multiple Touch Points</span></span>

<span data-ttu-id="5ec68-107">下列步驟說明如何使用 Windows Touch 來追蹤多個觸控點。</span><span class="sxs-lookup"><span data-stu-id="5ec68-107">The following steps explain how to track multiple touch points using Windows Touch.</span></span>

1.  <span data-ttu-id="5ec68-108">建立應用程式並啟用 Windows Touch。</span><span class="sxs-lookup"><span data-stu-id="5ec68-108">Create an application and enable Windows Touch.</span></span>
2.  <span data-ttu-id="5ec68-109">為 [**WM \_ 觸控**](wm-touchdown.md) 和追蹤點新增處理常式。</span><span class="sxs-lookup"><span data-stu-id="5ec68-109">Add a handler for [**WM\_TOUCH**](wm-touchdown.md) and track points.</span></span>
3.  <span data-ttu-id="5ec68-110">繪製點。</span><span class="sxs-lookup"><span data-stu-id="5ec68-110">Draw the points.</span></span>

<span data-ttu-id="5ec68-111">當您的應用程式執行之後，它會在每個觸控下呈現圓形。</span><span class="sxs-lookup"><span data-stu-id="5ec68-111">After you have your application running, it will render circles under each touch.</span></span> <span data-ttu-id="5ec68-112">下列螢幕擷取畫面會顯示您的應用程式在執行時的外觀。</span><span class="sxs-lookup"><span data-stu-id="5ec68-112">The following screen shot shows how your application might look while running.</span></span>

![顯示將觸控點轉譯為綠色和黃色圓形的應用程式螢幕擷取畫面](images/multitouchpoints.png)

## <a name="create-an-application-and-enable-windows-touch"></a><span data-ttu-id="5ec68-114">建立應用程式並啟用 Windows Touch</span><span class="sxs-lookup"><span data-stu-id="5ec68-114">Create an Application and Enable Windows Touch</span></span>

<span data-ttu-id="5ec68-115">使用 Microsoft Visual Studio wizard，從 Microsoft Win32 應用程式開始。</span><span class="sxs-lookup"><span data-stu-id="5ec68-115">Start with a Microsoft Win32 application using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="5ec68-116">當您完成嚮導之後，請在 targetver.h 中設定 Windows 版本，並在應用程式中包含 windows .h 和 windowsx，以新增 Windows Touch 訊息的支援。</span><span class="sxs-lookup"><span data-stu-id="5ec68-116">After you have completed the wizard, add support for Windows Touch messages by setting the Windows version in targetver.h and including windows.h and windowsx.h in your application.</span></span> <span data-ttu-id="5ec68-117">下列程式碼顯示如何在 targetver.h 中設定 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="5ec68-117">The following code shows how to set the Windows version in targetver.h.</span></span>


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



<span data-ttu-id="5ec68-118">下列程式碼顯示如何加入 include 指示詞。</span><span class="sxs-lookup"><span data-stu-id="5ec68-118">The following code shows how your include directives should be added.</span></span> <span data-ttu-id="5ec68-119">此外，您可以建立一些稍後將使用的全域變數。</span><span class="sxs-lookup"><span data-stu-id="5ec68-119">Also, you can create some global variables that will be used later.</span></span>


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



## <a name="add-handler-for-wm_touch-and-track-points"></a><span data-ttu-id="5ec68-120">為 WM \_ 觸控和追蹤點新增處理常式</span><span class="sxs-lookup"><span data-stu-id="5ec68-120">Add Handler for WM\_TOUCH and Track Points</span></span>

<span data-ttu-id="5ec68-121">首先，宣告 [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))中的 [**WM \_ 觸控**](wm-touchdown.md)處理常式所使用的一些變數。</span><span class="sxs-lookup"><span data-stu-id="5ec68-121">First, declare some variables that are used by the [**WM\_TOUCH**](wm-touchdown.md) handler in [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).</span></span>


```C++
int wmId, wmEvent, i, x, y;

UINT cInputs;
PTOUCHINPUT pInputs;
POINT ptInput;   
```



<span data-ttu-id="5ec68-122">現在，初始化用來儲存觸控點的變數，並從 **InitInstance** 方法註冊觸控輸入的視窗。</span><span class="sxs-lookup"><span data-stu-id="5ec68-122">Now, initialize the variables used for storing touch points and register the window for touch input from the **InitInstance** method.</span></span>


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



<span data-ttu-id="5ec68-123">接下來，從 [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))方法處理 [**WM \_ 觸控**](wm-touchdown.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="5ec68-123">Next, handle the [**WM\_TOUCH**](wm-touchdown.md) message from the [**WndProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) method.</span></span> <span data-ttu-id="5ec68-124">下列程式碼顯示適用于 **WM \_ 觸控** 的處理常式的執行。</span><span class="sxs-lookup"><span data-stu-id="5ec68-124">The following code shows an implementation of the handler for **WM\_TOUCH**.</span></span>


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
> <span data-ttu-id="5ec68-125">若要使用 [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) 函式，您的應用程式中必須有高 DPI 支援。</span><span class="sxs-lookup"><span data-stu-id="5ec68-125">In order to use the [**ScreenToClient**](/windows/desktop/api/winuser/nf-winuser-screentoclient) function, you must have high DPI support in your application.</span></span> <span data-ttu-id="5ec68-126">如需有關支援高 DPI 的詳細資訊，請參閱 MSDN 的 [高 DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) 區段。</span><span class="sxs-lookup"><span data-stu-id="5ec68-126">For more information on supporting high DPI, see the [High DPI]( ../hidpi/high-dpi-desktop-application-development-on-windows.md) section of MSDN.</span></span>

 

<span data-ttu-id="5ec68-127">現在當使用者接觸螢幕時，他或她所觸及的位置將會儲存在點陣列中。</span><span class="sxs-lookup"><span data-stu-id="5ec68-127">Now when a user touches the screen, the positions that he or she is touching will be stored in the points array.</span></span> <span data-ttu-id="5ec68-128">[**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput)結構的 **dwID** 成員會儲存與硬體相依的識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ec68-128">The **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure stores an identifier that will be hardware dependent.</span></span>

<span data-ttu-id="5ec68-129">為了解決 dwID 成員相依于硬體的問題， [**WM \_ 觸控**](wm-touchdown.md)案例處理常式會使用 **GetContactIndex** 的函式，將 [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput)結構的 **dwID** 成員對應至在螢幕上繪製的點。</span><span class="sxs-lookup"><span data-stu-id="5ec68-129">To address the issue of the dwID member being dependent on hardware, the [**WM\_TOUCH**](wm-touchdown.md) case handler uses a function, **GetContactIndex**, that maps the **dwID** member of the [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) structure to a point that is drawn on the screen.</span></span> <span data-ttu-id="5ec68-130">下列程式碼顯示此函式的實作為。</span><span class="sxs-lookup"><span data-stu-id="5ec68-130">The following code shows an implementation of this function.</span></span>


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



## <a name="draw-the-points"></a><span data-ttu-id="5ec68-131">繪製點</span><span class="sxs-lookup"><span data-stu-id="5ec68-131">Draw the Points</span></span>

<span data-ttu-id="5ec68-132">為繪圖常式宣告下列變數。</span><span class="sxs-lookup"><span data-stu-id="5ec68-132">Declare the following variables for the drawing routine.</span></span>


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



<span data-ttu-id="5ec68-133">記憶體顯示內容 *memDC* 是用來儲存暫存圖形內容，此內容會與轉譯的顯示內容（ *hdc*）交換以消除閃爍。</span><span class="sxs-lookup"><span data-stu-id="5ec68-133">The memory display context *memDC* is used for storing a temporary graphics context that is swapped with the rendered display context, *hdc*, to eliminate flickering.</span></span> <span data-ttu-id="5ec68-134">執行繪圖常式，以取得您所儲存的點，並在點繪製圓形。</span><span class="sxs-lookup"><span data-stu-id="5ec68-134">Implement the drawing routine, which takes the points you have stored and draws a circle at the points.</span></span> <span data-ttu-id="5ec68-135">下列程式碼顯示如何執行 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 處理常式。</span><span class="sxs-lookup"><span data-stu-id="5ec68-135">The following code shows how you could implement the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) handler.</span></span>


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



<span data-ttu-id="5ec68-136">當您執行應用程式時，它現在應該看起來像是本節開頭的圖例。</span><span class="sxs-lookup"><span data-stu-id="5ec68-136">When you run your application, it now should look something like the illustration at the beginning of this section.</span></span>

<span data-ttu-id="5ec68-137">有趣的是，您可以在觸控點周圍繪製一些額外的線。</span><span class="sxs-lookup"><span data-stu-id="5ec68-137">For fun, you can draw some extra lines around the touch points.</span></span> <span data-ttu-id="5ec68-138">下列螢幕擷取畫面顯示應用程式如何查看在圓形周圍繪製的一些額外的線。</span><span class="sxs-lookup"><span data-stu-id="5ec68-138">The following screen shot shows how the application could look with a few extra lines drawn around the circles.</span></span>

![顯示應用程式的螢幕擷取畫面，可將觸控點轉譯為具有直線的圓形，並與觸控點的邊緣相交](images/multitouchpointsfun.png)

## <a name="related-topics"></a><span data-ttu-id="5ec68-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ec68-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ec68-141">Windows Touch 輸入</span><span class="sxs-lookup"><span data-stu-id="5ec68-141">Windows Touch Input</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

 