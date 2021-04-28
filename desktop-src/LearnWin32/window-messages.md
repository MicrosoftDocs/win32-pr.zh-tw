---
title: 使用 Win32 和 c + +) 開始的視窗訊息 (
description: 使用 Win32 和 c + +) 開始的視窗訊息 (
ms.assetid: 90c20456-44ed-4f0f-a6d3-b6c5660f0bc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c00da564396e0f95947e33fb7d8db8b217ac5cdf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103836"
---
# <a name="window-messages-get-started-with-win32-and-c"></a><span data-ttu-id="1f220-103">使用 Win32 和 c + +) 開始的視窗訊息 (</span><span class="sxs-lookup"><span data-stu-id="1f220-103">Window Messages (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="1f220-104">GUI 應用程式必須回應來自使用者和作業系統的事件。</span><span class="sxs-lookup"><span data-stu-id="1f220-104">A GUI application must respond to events from the user and from the operating system.</span></span>

- <span data-ttu-id="1f220-105">**來自使用者的事件** 包括所有人都可以與您的程式互動的方式：按一下滑鼠、按鍵筆劃、觸控畫面手勢等等。</span><span class="sxs-lookup"><span data-stu-id="1f220-105">**Events from the user** include all the ways that someone can interact with your program: mouse clicks, key strokes, touch-screen gestures, and so on.</span></span>
- <span data-ttu-id="1f220-106">**作業系統中的事件** 包含程式的任何「外部」，可能會影響程式的運作方式。</span><span class="sxs-lookup"><span data-stu-id="1f220-106">**Events from the operating system** include anything "outside" of the program that can affect how the program behaves.</span></span> <span data-ttu-id="1f220-107">例如，使用者可能會插入新的硬體裝置，或 Windows 可能會進入較低電源狀態 (睡眠或休眠) 。</span><span class="sxs-lookup"><span data-stu-id="1f220-107">For example, the user might plug in a new hardware device, or Windows might enter a lower-power state (sleep or hibernate).</span></span>

<span data-ttu-id="1f220-108">這些事件可能會在程式執行時的任何時間，以幾乎任何順序發生。</span><span class="sxs-lookup"><span data-stu-id="1f220-108">These events can occur at any time while the program is running, in almost any order.</span></span> <span data-ttu-id="1f220-109">您如何建立程式，使其執行流程無法事先預測？</span><span class="sxs-lookup"><span data-stu-id="1f220-109">How do you structure a program whose flow of execution cannot be predicted in advance?</span></span>

<span data-ttu-id="1f220-110">為了解決這個問題，Windows 使用訊息傳遞模型。</span><span class="sxs-lookup"><span data-stu-id="1f220-110">To solve this problem, Windows uses a message-passing model.</span></span> <span data-ttu-id="1f220-111">作業系統會將訊息傳遞給應用程式視窗，以與您的應用程式視窗進行通訊。</span><span class="sxs-lookup"><span data-stu-id="1f220-111">The operating system communicates with your application window by passing messages to it.</span></span> <span data-ttu-id="1f220-112">訊息只是指定特定事件的數值代碼。</span><span class="sxs-lookup"><span data-stu-id="1f220-112">A message is simply a numeric code that designates a particular event.</span></span> <span data-ttu-id="1f220-113">例如，如果使用者按下滑鼠左鍵，則視窗會收到具有下列訊息碼的訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-113">For example, if the user presses the left mouse button, the window receives a message that has the following message code.</span></span>

```C++
#define WM_LBUTTONDOWN    0x0201
```

<span data-ttu-id="1f220-114">有些訊息有與其相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="1f220-114">Some messages have data associated with them.</span></span> <span data-ttu-id="1f220-115">例如， [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息包含滑鼠游標的 x 座標和 y 座標。</span><span class="sxs-lookup"><span data-stu-id="1f220-115">For example, the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message includes the x-coordinate and y-coordinate of the mouse cursor.</span></span>

<span data-ttu-id="1f220-116">為了將訊息傳遞至視窗，作業系統會呼叫為該視窗註冊的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="1f220-116">To pass a message to a window, the operating system calls the window procedure registered for that window.</span></span> <span data-ttu-id="1f220-117"> (，現在您知道視窗程式的用途。 ) </span><span class="sxs-lookup"><span data-stu-id="1f220-117">(And now you know what the window procedure is for.)</span></span>

## <a name="the-message-loop"></a><span data-ttu-id="1f220-118">訊息迴圈</span><span class="sxs-lookup"><span data-stu-id="1f220-118">The Message Loop</span></span>

<span data-ttu-id="1f220-119">應用程式會在執行時接收數以千計的訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-119">An application will receive thousands of messages while it runs.</span></span> <span data-ttu-id="1f220-120"> (考慮每個按鍵和滑鼠按鍵的點擊都會產生一則訊息。此外，) 此外，應用程式也可以有數個視窗，每個視窗都有自己的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="1f220-120">(Consider that every keystroke and mouse-button click generates a message.) Additionally, an application can have several windows, each with its own window procedure.</span></span> <span data-ttu-id="1f220-121">程式如何接收所有這些訊息，並將它們傳遞至正確的視窗程式？</span><span class="sxs-lookup"><span data-stu-id="1f220-121">How does the program receive all these messages and deliver them to the correct window procedure?</span></span> <span data-ttu-id="1f220-122">應用程式需要迴圈來取出訊息，並將它們分派至正確的視窗。</span><span class="sxs-lookup"><span data-stu-id="1f220-122">The application needs a loop to retrieve the messages and dispatch them to the correct windows.</span></span>

<span data-ttu-id="1f220-123">針對每個建立視窗的執行緒，作業系統會建立視窗訊息的佇列。</span><span class="sxs-lookup"><span data-stu-id="1f220-123">For each thread that creates a window, the operating system creates a queue for window messages.</span></span> <span data-ttu-id="1f220-124">此佇列會保留在該執行緒上建立之所有視窗的訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-124">This queue holds messages for all the windows that are created on that thread.</span></span> <span data-ttu-id="1f220-125">佇列本身在您的程式中是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="1f220-125">The queue itself is hidden from your program.</span></span> <span data-ttu-id="1f220-126">您無法直接操作佇列。</span><span class="sxs-lookup"><span data-stu-id="1f220-126">You cannot manipulate the queue directly.</span></span> <span data-ttu-id="1f220-127">不過，您可以藉由呼叫 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 函數，從佇列提取訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-127">However, you can pull a message from the queue by calling the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) function.</span></span>

```C++
MSG msg;
GetMessage(&msg, NULL, 0, 0);
```

<span data-ttu-id="1f220-128">此函式會從佇列的標頭中移除第一則訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-128">This function removes the first message from the head of the queue.</span></span> <span data-ttu-id="1f220-129">如果佇列是空的，則函式會封鎖，直到另一個訊息排入佇列為止。</span><span class="sxs-lookup"><span data-stu-id="1f220-129">If the queue is empty, the function blocks until another message is queued.</span></span> <span data-ttu-id="1f220-130">[**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)組塊的事實不會讓您的程式沒有回應。</span><span class="sxs-lookup"><span data-stu-id="1f220-130">The fact that [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) blocks will not make your program unresponsive.</span></span> <span data-ttu-id="1f220-131">如果沒有任何訊息，程式就不需要執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="1f220-131">If there are no messages, there is nothing for the program to do.</span></span> <span data-ttu-id="1f220-132">如果您必須執行背景處理，則可以建立其他執行緒，在 **GetMessage** 等候其他訊息時繼續執行。</span><span class="sxs-lookup"><span data-stu-id="1f220-132">If you have to perform background processing, you can create additional threads that continue to run while **GetMessage** waits for another message.</span></span> <span data-ttu-id="1f220-133"> (請參閱 [避免視窗程式中的瓶頸](writing-the-window-procedure.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="1f220-133">(See [Avoiding Bottlenecks in Your Window Procedure](writing-the-window-procedure.md).)</span></span>

<span data-ttu-id="1f220-134">[**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)的第一個參數是 [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="1f220-134">The first parameter of [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) is the address of a [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span> <span data-ttu-id="1f220-135">如果函式成功，它會將訊息的相關資訊填入 **訊息結構中** 。</span><span class="sxs-lookup"><span data-stu-id="1f220-135">If the function succeeds, it fills in the **MSG** structure with information about the message.</span></span> <span data-ttu-id="1f220-136">這包括目標視窗和訊息碼。</span><span class="sxs-lookup"><span data-stu-id="1f220-136">This includes the target window and the message code.</span></span> <span data-ttu-id="1f220-137">另外三個參數可讓您篩選從佇列取得的訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-137">The other three parameters let you filter which messages you get from the queue.</span></span> <span data-ttu-id="1f220-138">在幾乎所有情況下，您都會將這些參數設定為零。</span><span class="sxs-lookup"><span data-stu-id="1f220-138">In almost all cases, you will set these parameters to zero.</span></span>

<span data-ttu-id="1f220-139">雖然 [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) 結構包含訊息的相關資訊，但您幾乎不會直接檢查此結構。</span><span class="sxs-lookup"><span data-stu-id="1f220-139">Although the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure contains information about the message, you will almost never examine this structure directly.</span></span> <span data-ttu-id="1f220-140">相反地，您會將它直接傳遞給其他兩個函數。</span><span class="sxs-lookup"><span data-stu-id="1f220-140">Instead, you will pass it directly to two other functions.</span></span>

```C++
TranslateMessage(&msg); 
DispatchMessage(&msg);
```

<span data-ttu-id="1f220-141">[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)函數與鍵盤輸入相關。</span><span class="sxs-lookup"><span data-stu-id="1f220-141">The [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function is related to keyboard input.</span></span> <span data-ttu-id="1f220-142">它會將按鍵 (鍵向下轉譯按鍵，並將按鍵) 為字元。</span><span class="sxs-lookup"><span data-stu-id="1f220-142">It translates keystrokes (key down, key up) into characters.</span></span> <span data-ttu-id="1f220-143">您實際上不需要知道此函式的運作方式。請記得在 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)之前呼叫它。</span><span class="sxs-lookup"><span data-stu-id="1f220-143">You do not really have to know how this function works; just remember to call it before [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="1f220-144">如果您有好奇，MSDN 檔的連結將會提供更多資訊。</span><span class="sxs-lookup"><span data-stu-id="1f220-144">The link to the MSDN documentation will give you more information, if you are curious.</span></span>

<span data-ttu-id="1f220-145">[**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)函式會告知作業系統呼叫訊息目標視窗的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="1f220-145">The [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function tells the operating system to call the window procedure of the window that is the target of the message.</span></span> <span data-ttu-id="1f220-146">換句話說，作業系統會在其視窗的表格中查閱視窗控制碼、尋找與視窗相關聯的函式指標，以及叫用函數。</span><span class="sxs-lookup"><span data-stu-id="1f220-146">In other words, the operating system looks up the window handle in its table of windows, finds the function pointer associated with the window, and invokes the function.</span></span>

<span data-ttu-id="1f220-147">例如，假設使用者按下滑鼠左鍵。</span><span class="sxs-lookup"><span data-stu-id="1f220-147">For example, suppose that the user presses the left mouse button.</span></span> <span data-ttu-id="1f220-148">這會造成一連串的事件：</span><span class="sxs-lookup"><span data-stu-id="1f220-148">This causes a chain of events:</span></span>

1. <span data-ttu-id="1f220-149">作業系統會將 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) 訊息放在訊息佇列上。</span><span class="sxs-lookup"><span data-stu-id="1f220-149">The operating system puts a [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message on the message queue.</span></span>
2. <span data-ttu-id="1f220-150">您的程式會呼叫 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="1f220-150">Your program calls the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) function.</span></span>
3. <span data-ttu-id="1f220-151">[**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage)會從佇列提取 [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)訊息，並填滿訊息 [**結構。**](/windows/win32/api/winuser/ns-winuser-msg)</span><span class="sxs-lookup"><span data-stu-id="1f220-151">[**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) pulls the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message from the queue and fills in the [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure.</span></span>
4. <span data-ttu-id="1f220-152">您的程式會呼叫 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 和 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="1f220-152">Your program calls the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) functions.</span></span>
5. <span data-ttu-id="1f220-153">在 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)內，作業系統會呼叫您的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="1f220-153">Inside [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), the operating system calls your window procedure.</span></span>
6. <span data-ttu-id="1f220-154">您的視窗程式可以回應或忽略該訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-154">Your window procedure can either respond to the message or ignore it.</span></span>

<span data-ttu-id="1f220-155">當視窗程式傳回時，它會返回 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)。</span><span class="sxs-lookup"><span data-stu-id="1f220-155">When the window procedure returns, it returns back to [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="1f220-156">這會回到下一個訊息的訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="1f220-156">This returns to the message loop for the next message.</span></span> <span data-ttu-id="1f220-157">只要您的程式正在執行，訊息就會繼續抵達佇列。</span><span class="sxs-lookup"><span data-stu-id="1f220-157">As long as your program is running, messages will continue to arrive on the queue.</span></span> <span data-ttu-id="1f220-158">因此，您必須有迴圈，以持續從佇列提取訊息並分派訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-158">Therefore, you must have a loop that continually pulls messages from the queue and dispatches them.</span></span> <span data-ttu-id="1f220-159">您可以將迴圈視為進行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1f220-159">You can think of the loop as doing the following:</span></span>

```C++
// WARNING: Don't actually write your loop this way.

while (1)      
{
    GetMessage(&msg, NULL, 0,  0);
    TranslateMessage(&msg); 
    DispatchMessage(&msg);
}
```

<span data-ttu-id="1f220-160">當然，這個迴圈永遠不會結束。</span><span class="sxs-lookup"><span data-stu-id="1f220-160">As written, of course, this loop would never end.</span></span> <span data-ttu-id="1f220-161">這是 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 函數的傳回值。</span><span class="sxs-lookup"><span data-stu-id="1f220-161">That is where the return value for the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) function comes in.</span></span> <span data-ttu-id="1f220-162">一般來說， **GetMessage** 會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="1f220-162">Normally, **GetMessage** returns a nonzero value.</span></span> <span data-ttu-id="1f220-163">當您想要結束應用程式並中斷訊息迴圈時，請呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) 函數。</span><span class="sxs-lookup"><span data-stu-id="1f220-163">When you want to exit the application and break out of the message loop, call the [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) function.</span></span>

```C++
        PostQuitMessage(0);
```

<span data-ttu-id="1f220-164">[**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)函式會在訊息佇列上放置 [**WM \_ 結束**](/windows/desktop/winmsg/wm-quit)訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-164">The [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) function puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue.</span></span> <span data-ttu-id="1f220-165">**WM \_QUIT** 是特殊訊息：它會使 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 傳回零，並在訊息迴圈結束時發出信號。</span><span class="sxs-lookup"><span data-stu-id="1f220-165">**WM\_QUIT** is a special message: It causes [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) to return zero, signaling the end of the message loop.</span></span> <span data-ttu-id="1f220-166">以下是修改過的訊息迴圈。</span><span class="sxs-lookup"><span data-stu-id="1f220-166">Here is the revised message loop.</span></span>

```C++
// Correct.

MSG msg = { };
while (GetMessage(&msg, NULL, 0, 0) > 0)
{
    TranslateMessage(&msg);
    DispatchMessage(&msg);
}
```

<span data-ttu-id="1f220-167">只要 [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 傳回非零值， **while** 迴圈中的運算式就會評估為 true。</span><span class="sxs-lookup"><span data-stu-id="1f220-167">As long as [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) returns a nonzero value, the expression in the **while** loop evaluates to true.</span></span> <span data-ttu-id="1f220-168">在您呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)之後，運算式會變成 false，而且程式會中斷迴圈。</span><span class="sxs-lookup"><span data-stu-id="1f220-168">After you call [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage), the expression becomes false and the program breaks out of the loop.</span></span> <span data-ttu-id="1f220-169">這種行為 (一個有趣的結果，就是您的視窗程式永遠不會收到 [**WM \_**](/windows/desktop/winmsg/wm-quit) 結束訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-169">(One interesting result of this behavior is that your window procedure never receives a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message.</span></span> <span data-ttu-id="1f220-170">因此，您在視窗程式中不需要有此訊息的 case 語句。 ) </span><span class="sxs-lookup"><span data-stu-id="1f220-170">Therefore, you do not have to have a case statement for this message in your window procedure.)</span></span>

<span data-ttu-id="1f220-171">下一個明顯的問題是呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)的時機。</span><span class="sxs-lookup"><span data-stu-id="1f220-171">The next obvious question is when to call [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span> <span data-ttu-id="1f220-172">我們會在 [關閉視窗](closing-the-window.md)的主題中返回這個問題，但是首先我們必須撰寫視窗程式。</span><span class="sxs-lookup"><span data-stu-id="1f220-172">We'll return to this question in the topic [Closing the Window](closing-the-window.md), but first we have to write our window procedure.</span></span>

## <a name="posted-messages-versus-sent-messages"></a><span data-ttu-id="1f220-173">張貼的訊息與傳送的訊息</span><span class="sxs-lookup"><span data-stu-id="1f220-173">Posted Messages versus Sent Messages</span></span>

<span data-ttu-id="1f220-174">上一節討論到佇列中的訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-174">The previous section talked about messages going onto a queue.</span></span> <span data-ttu-id="1f220-175">有時候，作業系統會直接呼叫視窗程式，略過佇列。</span><span class="sxs-lookup"><span data-stu-id="1f220-175">Sometimes, the operating system will call a window procedure directly, bypassing the queue.</span></span>

<span data-ttu-id="1f220-176">這種差異的術語可能會造成混淆：</span><span class="sxs-lookup"><span data-stu-id="1f220-176">The terminology for this distinction can be confusing:</span></span>

-   <span data-ttu-id="1f220-177">*張貼* 訊息表示訊息會進入訊息佇列，並透過訊息迴圈 ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) 和 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)) 來分派。</span><span class="sxs-lookup"><span data-stu-id="1f220-177">*Posting* a message means the message goes on the message queue, and is dispatched through the message loop ([**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)).</span></span>
-   <span data-ttu-id="1f220-178">傳送訊息表示訊息會略過佇列，而作業系統則會直接呼叫視窗程式。</span><span class="sxs-lookup"><span data-stu-id="1f220-178">*Sending* a message means the message skips the queue, and the operating system calls the window procedure directly.</span></span>

<span data-ttu-id="1f220-179">目前的差異並不重要。</span><span class="sxs-lookup"><span data-stu-id="1f220-179">For now, the difference is not very important.</span></span> <span data-ttu-id="1f220-180">視窗程式會處理所有訊息。</span><span class="sxs-lookup"><span data-stu-id="1f220-180">The window procedure handles all messages.</span></span> <span data-ttu-id="1f220-181">但是，有些訊息會略過佇列，並直接移至您的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="1f220-181">However, some messages bypass the queue and go directly to your window procedure.</span></span> <span data-ttu-id="1f220-182">但是，如果您的應用程式在 windows 之間進行通訊，它可能會有差異。</span><span class="sxs-lookup"><span data-stu-id="1f220-182">However, it can make a difference if your application communicates between windows.</span></span> <span data-ttu-id="1f220-183">您可以在 [有關訊息和訊息佇列](/windows/desktop/winmsg/about-messages-and-message-queues)的主題中找到此問題的更詳盡討論。</span><span class="sxs-lookup"><span data-stu-id="1f220-183">You can find a more thorough discussion of this issue in the topic [About Messages and Message Queues](/windows/desktop/winmsg/about-messages-and-message-queues).</span></span>

## <a name="next"></a><span data-ttu-id="1f220-184">下一個</span><span class="sxs-lookup"><span data-stu-id="1f220-184">Next</span></span>

[<span data-ttu-id="1f220-185">撰寫視窗程式</span><span class="sxs-lookup"><span data-stu-id="1f220-185">Writing the Window Procedure</span></span>](writing-the-window-procedure.md)
