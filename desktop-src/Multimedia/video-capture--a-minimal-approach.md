---
title: 影片捕獲的基本方法
description: 影片捕獲的基本方法
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- 適用于 Windows (VFW) 影片捕獲影片
- 適用于 Windows) 的 VFW (影片、影片捕獲
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842172"
---
# <a name="video-capture-a-minimal-approach"></a><span data-ttu-id="bd34c-105">影片捕獲：基本方法</span><span class="sxs-lookup"><span data-stu-id="bd34c-105">Video Capture: A Minimal Approach</span></span>

<span data-ttu-id="bd34c-106">影片捕獲 digitizes 影片和音訊資料的串流，並將其儲存在硬碟或其他類型的持續性儲存裝置上。</span><span class="sxs-lookup"><span data-stu-id="bd34c-106">Video capture digitizes a stream of video and audio data, and stores it on a hard disk or some other type of persistent storage device.</span></span> <span data-ttu-id="bd34c-107">本節說明如何使用三個程式碼語句，將簡單的影片捕獲形式新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="bd34c-107">This section describes how to add a simple form of video capture to an application using three statements of code.</span></span> <span data-ttu-id="bd34c-108">它也會說明如何藉由將訊息傳送至 [捕獲] 視窗來結束或中止捕獲會話。</span><span class="sxs-lookup"><span data-stu-id="bd34c-108">It also describes how to end or abort a capture session by sending messages to the capture window.</span></span>

<span data-ttu-id="bd34c-109">AVICap capture 視窗會處理將音訊和影片捕獲串流至 AVI 檔案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="bd34c-109">An AVICap capture window handles the details of streaming audio and video capture to AVI files.</span></span> <span data-ttu-id="bd34c-110">如此一來，您的應用程式就不會參與 AVI 檔案格式、影片和音訊緩衝區管理，以及影片和音訊裝置磁碟機的低層級存取。</span><span class="sxs-lookup"><span data-stu-id="bd34c-110">This frees your application from involvement in the AVI file format, video and audio buffer management, and the low-level access of video and audio device drivers.</span></span> <span data-ttu-id="bd34c-111">AVICap 為應用程式提供彈性的介面。</span><span class="sxs-lookup"><span data-stu-id="bd34c-111">AVICap provides a flexible interface for applications.</span></span> <span data-ttu-id="bd34c-112">您可以使用下列幾行程式碼，將影片捕獲新增至應用程式：</span><span class="sxs-lookup"><span data-stu-id="bd34c-112">You can add video capture to your application, using only the following lines of code:</span></span>


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



<span data-ttu-id="bd34c-113">也提供一個宏介面，可提供使用 [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) 函式的替代方法，並改善應用程式的可讀性。</span><span class="sxs-lookup"><span data-stu-id="bd34c-113">A macro interface is also available that provides an alternative to using the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function and improves the readability of an application.</span></span> <span data-ttu-id="bd34c-114">下列範例會使用宏介面，將影片捕獲新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="bd34c-114">The following example uses the macro interface to add video capture to an application.</span></span>


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



<span data-ttu-id="bd34c-115">當您的應用程式建立 AVICap 視窗類別的捕獲視窗，並將它連接至視頻驅動程式之後，[capture] 視窗就可以開始捕獲資料。</span><span class="sxs-lookup"><span data-stu-id="bd34c-115">After your application creates a capture window of the AVICap window class and connects it to a video driver, the capture window is ready to capture data.</span></span> <span data-ttu-id="bd34c-116">至此，您的應用程式可以直接傳送 [**WM \_ CAP \_ 序列**](wm-cap-sequence.md) 訊息 (或 [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) 宏) 來開始進行捕捉。</span><span class="sxs-lookup"><span data-stu-id="bd34c-116">At this point, your application can simply send the [**WM\_CAP\_SEQUENCE**](wm-cap-sequence.md) message (or the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro) to begin capturing.</span></span>

<span data-ttu-id="bd34c-117">在使用預設設定的情況下，會 \_ \_ 將影片和音訊輸入的捕獲起始至名為 CAPTURE.AVI 的檔案。</span><span class="sxs-lookup"><span data-stu-id="bd34c-117">Using default settings, WM\_CAP\_SEQUENCE initiates the capture of video and audio input to a file named CAPTURE.AVI.</span></span> <span data-ttu-id="bd34c-118">Capture 會繼續進行，直到發生下列其中一個事件為止：</span><span class="sxs-lookup"><span data-stu-id="bd34c-118">Capture continues until one of the following events occurs:</span></span>

-   <span data-ttu-id="bd34c-119">使用者按下 ESC 鍵或滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="bd34c-119">The user presses the ESC key or a mouse button.</span></span>
-   <span data-ttu-id="bd34c-120">您的應用程式會停止或中止捕獲操作。</span><span class="sxs-lookup"><span data-stu-id="bd34c-120">Your application stops or aborts capture operation.</span></span>
-   <span data-ttu-id="bd34c-121">磁片已滿。</span><span class="sxs-lookup"><span data-stu-id="bd34c-121">The disk becomes full.</span></span>

<span data-ttu-id="bd34c-122">在應用程式中，您可以藉由將 [**WM \_ CAP \_ Stop**](wm-cap-stop.md) (或 [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) 宏) 訊息傳送至「捕獲視窗」，來停止將捕獲的資料串流處理至檔案。</span><span class="sxs-lookup"><span data-stu-id="bd34c-122">In an application, you can stop streaming captured data to a file by sending the [**WM\_CAP\_STOP**](wm-cap-stop.md) (or the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro) message to a capture window.</span></span> <span data-ttu-id="bd34c-123">您也可以將 [**WM \_ CAP \_ abort**](wm-cap-abort.md) message (或 [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) 宏) 傳送至 capture 視窗，以中止捕捉作業。</span><span class="sxs-lookup"><span data-stu-id="bd34c-123">You can also abort the capture operation by sending the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message (or the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro) to a capture window.</span></span>

 

 