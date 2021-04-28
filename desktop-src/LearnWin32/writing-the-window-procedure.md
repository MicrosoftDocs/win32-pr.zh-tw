---
title: 撰寫視窗程式
description: 撰寫視窗程式
ms.assetid: f022bb88-6e4c-4ec4-9eef-f125ad92167e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832aba88211a7decf20c233f5d9ab4fbeb1b1c27
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105716"
---
# <a name="writing-the-window-procedure"></a><span data-ttu-id="16af1-103">撰寫視窗程式</span><span class="sxs-lookup"><span data-stu-id="16af1-103">Writing the Window Procedure</span></span>

<span data-ttu-id="16af1-104">[**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)函式會呼叫訊息目標視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="16af1-104">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function calls the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="16af1-105">視窗程式具有下列簽章。</span><span class="sxs-lookup"><span data-stu-id="16af1-105">The window procedure has the following signature.</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam);
```

<span data-ttu-id="16af1-106">有四個參數：</span><span class="sxs-lookup"><span data-stu-id="16af1-106">There are four parameters:</span></span>

- <span data-ttu-id="16af1-107">*hwnd* 是視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="16af1-107">*hwnd* is a handle to the window.</span></span>
- <span data-ttu-id="16af1-108">*uMsg* 是訊息代碼;例如， [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息表示視窗已調整大小。</span><span class="sxs-lookup"><span data-stu-id="16af1-108">*uMsg* is the message code; for example, the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message indicates the window was resized.</span></span>
- <span data-ttu-id="16af1-109">*wParam* 和 *lParam* 包含與訊息相關的其他資料。</span><span class="sxs-lookup"><span data-stu-id="16af1-109">*wParam* and *lParam* contain additional data that pertains to the message.</span></span> <span data-ttu-id="16af1-110">確切的意義取決於訊息碼。</span><span class="sxs-lookup"><span data-stu-id="16af1-110">The exact meaning depends on the message code.</span></span>

<span data-ttu-id="16af1-111">**LRESULT** 是您的程式傳回給 Windows 的整數值。</span><span class="sxs-lookup"><span data-stu-id="16af1-111">**LRESULT** is an integer value that your program returns to Windows.</span></span> <span data-ttu-id="16af1-112">它包含您的程式對特定訊息的回應。</span><span class="sxs-lookup"><span data-stu-id="16af1-112">It contains your program's response to a particular message.</span></span> <span data-ttu-id="16af1-113">此值的意義取決於訊息碼。</span><span class="sxs-lookup"><span data-stu-id="16af1-113">The meaning of this value depends on the message code.</span></span> <span data-ttu-id="16af1-114">**回呼** 是函數的呼叫慣例。</span><span class="sxs-lookup"><span data-stu-id="16af1-114">**CALLBACK** is the calling convention for the function.</span></span>

<span data-ttu-id="16af1-115">一般的視窗程式只是在訊息程式碼上切換的大型 switch 語句。</span><span class="sxs-lookup"><span data-stu-id="16af1-115">A typical window procedure is simply a large switch statement that switches on the message code.</span></span> <span data-ttu-id="16af1-116">針對您想要處理的每個訊息新增案例。</span><span class="sxs-lookup"><span data-stu-id="16af1-116">Add cases for each message that you want to handle.</span></span>

```C++
switch (uMsg)
{
    case WM_SIZE: // Handle window resizing

    // etc
}
```

<span data-ttu-id="16af1-117">訊息的額外資料會包含在 *lParam* 和 *wParam* 參數中。</span><span class="sxs-lookup"><span data-stu-id="16af1-117">Additional data for the message is contained in the *lParam* and *wParam* parameters.</span></span> <span data-ttu-id="16af1-118">這兩個參數都是整數值，也就是指標寬度的大小 (32 位或64位) 。</span><span class="sxs-lookup"><span data-stu-id="16af1-118">Both parameters are integer values the size of a pointer width (32 bits or 64 bits).</span></span> <span data-ttu-id="16af1-119">各項的意義取決於 (*uMsg*) 的訊息碼。</span><span class="sxs-lookup"><span data-stu-id="16af1-119">The meaning of each depends on the message code (*uMsg*).</span></span> <span data-ttu-id="16af1-120">針對每個訊息，您必須查閱 MSDN 上的訊息程式碼，並將參數轉換成正確的資料類型。</span><span class="sxs-lookup"><span data-stu-id="16af1-120">For each message, you will need to look up the message code on MSDN and cast the parameters to the correct data type.</span></span> <span data-ttu-id="16af1-121">資料通常是數值或結構的指標。</span><span class="sxs-lookup"><span data-stu-id="16af1-121">Usually the data is either a numeric value or a pointer to a structure.</span></span> <span data-ttu-id="16af1-122">某些訊息沒有任何資料。</span><span class="sxs-lookup"><span data-stu-id="16af1-122">Some messages do not have any data.</span></span>

<span data-ttu-id="16af1-123">例如， [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息的檔指出：</span><span class="sxs-lookup"><span data-stu-id="16af1-123">For example, the documentation for the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message states that:</span></span>

- <span data-ttu-id="16af1-124">*wParam* 是一個旗標，指出視窗是否最小化、最大化或調整大小。</span><span class="sxs-lookup"><span data-stu-id="16af1-124">*wParam* is a flag that indicates whether the window was minimized, maximized, or resized.</span></span>
- <span data-ttu-id="16af1-125">*lParam* 包含視窗的新寬度和高度，做為將16位值壓縮成 1 32 或64位數位。</span><span class="sxs-lookup"><span data-stu-id="16af1-125">*lParam* contains the new width and height of the window as 16-bit values packed into one 32- or 64-bit number.</span></span> <span data-ttu-id="16af1-126">您必須執行一些位移位以取得這些值。</span><span class="sxs-lookup"><span data-stu-id="16af1-126">You will need to perform some bit-shifting to get these values.</span></span> <span data-ttu-id="16af1-127">幸運的是，標頭檔 WinDef 包含可進行此作業的 helper 宏。</span><span class="sxs-lookup"><span data-stu-id="16af1-127">Fortunately, the header file WinDef.h includes helper macros that do this.</span></span>

<span data-ttu-id="16af1-128">一般的視窗程式會處理數十個訊息，因此它可能會變得很長。</span><span class="sxs-lookup"><span data-stu-id="16af1-128">A typical window procedure handles dozens of messages, so it can grow quite long.</span></span> <span data-ttu-id="16af1-129">讓您的程式碼更模組化的其中一種方式，是將處理每個訊息的邏輯放在個別的函式中。</span><span class="sxs-lookup"><span data-stu-id="16af1-129">One way to make your code more modular is to put the logic for handling each message in a separate function.</span></span> <span data-ttu-id="16af1-130">在視窗程式中，將 *wParam* 和 *lParam* 參數轉換成正確的資料類型，並將這些值傳遞至函式。</span><span class="sxs-lookup"><span data-stu-id="16af1-130">In the window procedure, cast the *wParam* and *lParam* parameters to the correct data type, and pass those values to the function.</span></span> <span data-ttu-id="16af1-131">例如，若要處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息，視窗程式如下所示：</span><span class="sxs-lookup"><span data-stu-id="16af1-131">For example, to handle the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message, the window procedure would look like this:</span></span>

```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_SIZE:
        {
            int width = LOWORD(lParam);  // Macro to get the low-order word.
            int height = HIWORD(lParam); // Macro to get the high-order word.

            // Respond to the message:
            OnSize(hwnd, (UINT)wParam, width, height);
        }
        break;
    }
}

void OnSize(HWND hwnd, UINT flag, int width, int height)
{
    // Handle resizing
}
```

<span data-ttu-id="16af1-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))和 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))宏會從 *lParam* 取得16位的寬度和高度值。</span><span class="sxs-lookup"><span data-stu-id="16af1-132">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) macros get the 16-bit width and height values from *lParam*.</span></span> <span data-ttu-id="16af1-133"> (您可以在 MSDN 檔中查看每個訊息代碼的這幾種詳細資料。 ) 視窗程式會將寬度和高度解壓縮，然後將這些值傳遞至函式 `OnSize` 。</span><span class="sxs-lookup"><span data-stu-id="16af1-133">(You can look up these kinds of details in the MSDN documentation for each message code.) The window procedure extracts the width and height, and then passes these values to the `OnSize` function.</span></span>

## <a name="default-message-handling"></a><span data-ttu-id="16af1-134">預設訊息處理</span><span class="sxs-lookup"><span data-stu-id="16af1-134">Default Message Handling</span></span>

<span data-ttu-id="16af1-135">如果您未處理視窗程式中的特定訊息，請將訊息參數直接傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函數。</span><span class="sxs-lookup"><span data-stu-id="16af1-135">If you don't handle a particular message in your window procedure, pass the message parameters directly to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span> <span data-ttu-id="16af1-136">此函式會執行訊息的預設動作，這會因訊息類型而異。</span><span class="sxs-lookup"><span data-stu-id="16af1-136">This function performs the default action for the message, which varies by message type.</span></span>

```C++
return DefWindowProc(hwnd, uMsg, wParam, lParam);
```

## <a name="avoiding-bottlenecks-in-your-window-procedure"></a><span data-ttu-id="16af1-137">避免視窗程式中的瓶頸</span><span class="sxs-lookup"><span data-stu-id="16af1-137">Avoiding Bottlenecks in Your Window Procedure</span></span>

<span data-ttu-id="16af1-138">當您的視窗程式執行時，它會封鎖在相同執行緒上建立之 windows 的任何其他訊息。</span><span class="sxs-lookup"><span data-stu-id="16af1-138">While your window procedure executes, it blocks any other messages for windows created on the same thread.</span></span> <span data-ttu-id="16af1-139">因此，請避免在您的視窗程式內進行冗長的處理。</span><span class="sxs-lookup"><span data-stu-id="16af1-139">Therefore, avoid lengthy processing inside your window procedure.</span></span> <span data-ttu-id="16af1-140">例如，假設您的程式開啟了 TCP 連線，並無限期等待伺服器回應。</span><span class="sxs-lookup"><span data-stu-id="16af1-140">For example, suppose your program opens a TCP connection and waits indefinitely for the server to respond.</span></span> <span data-ttu-id="16af1-141">如果您在視窗程式中這麼做，則在要求完成之前，您的 UI 將不會回應。</span><span class="sxs-lookup"><span data-stu-id="16af1-141">If you do that inside the window procedure, your UI will not respond until the request completes.</span></span> <span data-ttu-id="16af1-142">在這段時間內，視窗無法處理滑鼠或鍵盤輸入、重新繪製或甚至關閉。</span><span class="sxs-lookup"><span data-stu-id="16af1-142">During that time, the window cannot process mouse or keyboard input, repaint itself, or even close.</span></span>

<span data-ttu-id="16af1-143">相反地，您應該使用 Windows 內建的多工工具之一，將工作移至另一個執行緒：</span><span class="sxs-lookup"><span data-stu-id="16af1-143">Instead, you should move the work to another thread, using one of the multitasking facilities that are built into Windows:</span></span>

- <span data-ttu-id="16af1-144">建立新的執行緒。</span><span class="sxs-lookup"><span data-stu-id="16af1-144">Create a new thread.</span></span>
- <span data-ttu-id="16af1-145">使用執行緒集區。</span><span class="sxs-lookup"><span data-stu-id="16af1-145">Use a thread pool.</span></span>
- <span data-ttu-id="16af1-146">使用非同步 i/o 呼叫。</span><span class="sxs-lookup"><span data-stu-id="16af1-146">Use asynchronous I/O calls.</span></span>
- <span data-ttu-id="16af1-147">使用非同步程序呼叫。</span><span class="sxs-lookup"><span data-stu-id="16af1-147">Use asynchronous procedure calls.</span></span>

## <a name="next"></a><span data-ttu-id="16af1-148">下一個</span><span class="sxs-lookup"><span data-stu-id="16af1-148">Next</span></span>

[<span data-ttu-id="16af1-149">繪製視窗</span><span class="sxs-lookup"><span data-stu-id="16af1-149">Painting the Window</span></span>](painting-the-window.md)
