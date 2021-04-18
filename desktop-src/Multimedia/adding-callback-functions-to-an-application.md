---
title: 將回呼函式加入至應用程式
description: 將回呼函式加入至應用程式
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f5f3dc43227f92305032decaf917bf521d95b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507252"
---
# <a name="adding-callback-functions-to-an-application"></a><span data-ttu-id="11912-103">將回呼函式加入至應用程式</span><span class="sxs-lookup"><span data-stu-id="11912-103">Adding Callback Functions to an Application</span></span>

<span data-ttu-id="11912-104">應用程式可以使用捕捉視窗註冊回呼函式，以便在下列情況下通知應用程式：</span><span class="sxs-lookup"><span data-stu-id="11912-104">An application can register callback functions with the capture window so that it notifies the application in the following circumstances:</span></span>

-   <span data-ttu-id="11912-105">狀態變更</span><span class="sxs-lookup"><span data-stu-id="11912-105">The status changes</span></span>
-   <span data-ttu-id="11912-106">發生錯誤</span><span class="sxs-lookup"><span data-stu-id="11912-106">Errors occur</span></span>
-   <span data-ttu-id="11912-107">影片畫面和音訊緩衝區變成可用</span><span class="sxs-lookup"><span data-stu-id="11912-107">Video frame and audio buffers become available</span></span>
-   <span data-ttu-id="11912-108">應用程式應該在串流捕獲期間產生</span><span class="sxs-lookup"><span data-stu-id="11912-108">The application should yield during streaming capture</span></span>

<span data-ttu-id="11912-109">下列範例會建立一個捕獲視窗，並在應用程式的訊息處理迴圈中註冊狀態、錯誤、影片串流和框架回呼函式。</span><span class="sxs-lookup"><span data-stu-id="11912-109">The following example creates a capture window and registers status, error, video stream, and frame callback functions in the message-processing loop of an application.</span></span> <span data-ttu-id="11912-110">它也包含停用回呼函數的範例語句。</span><span class="sxs-lookup"><span data-stu-id="11912-110">It also includes a sample statement for disabling a callback function.</span></span> <span data-ttu-id="11912-111">後續範例會顯示簡單狀態、錯誤和框架回呼函式。</span><span class="sxs-lookup"><span data-stu-id="11912-111">Subsequent examples show simple status, error, and frame callback functions.</span></span>


```C++
case WM_CREATE: 
{ 
    char    achDeviceName[80] ; 
    char    achDeviceVersion[100] ; 
    char    achBuffer[100] ; 
    WORD    wDriverCount = 0 ; 
    WORD    wIndex ; 
    WORD    wError ; 
    HMENU   hMenu ; 
 
    // Create a capture window using the capCreateCaptureWindow macro.
    ghWndCap = capCreateCaptureWindow((LPSTR)"Capture Window", 
        WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, (HWND) hWnd, (int) 0); 
 
    // Register the error callback function using the 
    // capSetCallbackOnError macro. 
    capSetCallbackOnError(ghWndCap, fpErrorCallback); 
 
    // Register the status callback function using the 
    // capSetCallbackOnStatus macro. 
    capSetCallbackOnStatus(ghWndCap, fpStatusCallback); 
 
    // Register the video-stream callback function using the
    // capSetCallbackOnVideoStream macro. 
    capSetCallbackOnVideoStream(ghWndCap, fpVideoCallback); 
 
    // Register the frame callback function using the
    // capSetCallbackOnFrame macro. 
    capSetCallbackOnFrame(ghWndCap, fpFrameCallback); 
 
    // Connect to a capture driver 

    break; 
} 
case WM_CLOSE: 
{ 
// Use the capSetCallbackOnFrame macro to 
// disable the frame callback. Similar calls exist for the other 
// callback functions.

    capSetCallbackOnFrame(ghWndCap, NULL); 

    break; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="11912-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="11912-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11912-113">使用影片捕獲</span><span class="sxs-lookup"><span data-stu-id="11912-113">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




