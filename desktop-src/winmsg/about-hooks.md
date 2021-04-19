---
description: 本主題討論如何使用勾點。
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: 攔截
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c5d89f111604418d1dc3ea9a4ebce6fe0a8124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975400"
---
# <a name="hooks-overview"></a><span data-ttu-id="1b36e-103">攔截</span><span class="sxs-lookup"><span data-stu-id="1b36e-103">Hooks Overview</span></span>

<span data-ttu-id="1b36e-104">攔截 *器是一* 種機制，可讓應用程式攔截事件，例如訊息、滑鼠動作和按鍵。</span><span class="sxs-lookup"><span data-stu-id="1b36e-104">A *hook* is a mechanism by which an application can intercept events, such as messages, mouse actions, and keystrokes.</span></span> <span data-ttu-id="1b36e-105">攔截特定事件種類的函式稱為攔截 *程式。*</span><span class="sxs-lookup"><span data-stu-id="1b36e-105">A function that intercepts a particular type of event is known as a *hook procedure*.</span></span> <span data-ttu-id="1b36e-106">攔截程式可以對它收到的每個事件採取動作，然後修改或捨棄事件。</span><span class="sxs-lookup"><span data-stu-id="1b36e-106">A hook procedure can act on each event it receives, and then modify or discard the event.</span></span>

<span data-ttu-id="1b36e-107">下列範例會使用於攔截：</span><span class="sxs-lookup"><span data-stu-id="1b36e-107">The following some example uses for hooks:</span></span>

-   <span data-ttu-id="1b36e-108">監視訊息以進行調試</span><span class="sxs-lookup"><span data-stu-id="1b36e-108">Monitor messages for debugging purposes</span></span>
-   <span data-ttu-id="1b36e-109">提供宏錄製和播放的支援</span><span class="sxs-lookup"><span data-stu-id="1b36e-109">Provide support for recording and playback of macros</span></span>
-   <span data-ttu-id="1b36e-110">提供 help 鍵支援 (F1) </span><span class="sxs-lookup"><span data-stu-id="1b36e-110">Provide support for a help key (F1)</span></span>
-   <span data-ttu-id="1b36e-111">模擬滑鼠和鍵盤輸入</span><span class="sxs-lookup"><span data-stu-id="1b36e-111">Simulate mouse and keyboard input</span></span>
-   <span data-ttu-id="1b36e-112">執行以電腦為基礎的訓練 (CBT) 應用程式</span><span class="sxs-lookup"><span data-stu-id="1b36e-112">Implement a computer-based training (CBT) application</span></span>

> [!Note]  
> <span data-ttu-id="1b36e-113">攔截通常會讓系統變慢，因為它們會增加系統必須針對每個訊息執行的處理量。</span><span class="sxs-lookup"><span data-stu-id="1b36e-113">Hooks tend to slow down the system because they increase the amount of processing the system must perform for each message.</span></span> <span data-ttu-id="1b36e-114">您應該只在必要時才安裝攔截，並儘快將它移除。</span><span class="sxs-lookup"><span data-stu-id="1b36e-114">You should install a hook only when necessary, and remove it as soon as possible.</span></span>

 

<span data-ttu-id="1b36e-115">本節將討論下列各項：</span><span class="sxs-lookup"><span data-stu-id="1b36e-115">This section discusses the following:</span></span>

-   [<span data-ttu-id="1b36e-116">攔截鏈</span><span class="sxs-lookup"><span data-stu-id="1b36e-116">Hook Chains</span></span>](#hook-chains)
-   [<span data-ttu-id="1b36e-117">攔截程式</span><span class="sxs-lookup"><span data-stu-id="1b36e-117">Hook Procedures</span></span>](#hook-procedures)
-   [<span data-ttu-id="1b36e-118">掛勾類型</span><span class="sxs-lookup"><span data-stu-id="1b36e-118">Hook Types</span></span>](#hook-types)
    -   [<span data-ttu-id="1b36e-119">WH \_ CALLWNDPROC 和 WH \_ CALLWNDPROCRET</span><span class="sxs-lookup"><span data-stu-id="1b36e-119">WH\_CALLWNDPROC and WH\_CALLWNDPROCRET</span></span>](#wh_callwndproc-and-wh_callwndprocret)
    -   [<span data-ttu-id="1b36e-120">WH \_ CBT</span><span class="sxs-lookup"><span data-stu-id="1b36e-120">WH\_CBT</span></span>](#wh_cbt)
    -   [<span data-ttu-id="1b36e-121">WH \_ DEBUG</span><span class="sxs-lookup"><span data-stu-id="1b36e-121">WH\_DEBUG</span></span>](#wh_debug)
    -   [<span data-ttu-id="1b36e-122">WH \_ FOREGROUNDIDLE</span><span class="sxs-lookup"><span data-stu-id="1b36e-122">WH\_FOREGROUNDIDLE</span></span>](#wh_foregroundidle)
    -   [<span data-ttu-id="1b36e-123">WH \_ GETMESSAGE</span><span class="sxs-lookup"><span data-stu-id="1b36e-123">WH\_GETMESSAGE</span></span>](#wh_getmessage)
    -   [<span data-ttu-id="1b36e-124">WH \_ JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="1b36e-124">WH\_JOURNALPLAYBACK</span></span>](#wh_journalplayback)
    -   [<span data-ttu-id="1b36e-125">WH \_ JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="1b36e-125">WH\_JOURNALRECORD</span></span>](#wh_journalrecord)
    -   [<span data-ttu-id="1b36e-126">WH \_ 鍵盤 \_ LL</span><span class="sxs-lookup"><span data-stu-id="1b36e-126">WH\_KEYBOARD\_LL</span></span>](#wh_keyboard_ll)
    -   [<span data-ttu-id="1b36e-127">WH \_ 鍵盤</span><span class="sxs-lookup"><span data-stu-id="1b36e-127">WH\_KEYBOARD</span></span>](#wh_keyboard)
    -   [<span data-ttu-id="1b36e-128">WH \_ 滑鼠 \_ LL</span><span class="sxs-lookup"><span data-stu-id="1b36e-128">WH\_MOUSE\_LL</span></span>](#wh_mouse_ll)
    -   [<span data-ttu-id="1b36e-129">WH \_ 滑鼠</span><span class="sxs-lookup"><span data-stu-id="1b36e-129">WH\_MOUSE</span></span>](#wh_mouse)
    -   [<span data-ttu-id="1b36e-130">WH \_ MSGFILTER 和 WH \_ SYSMSGFILTER</span><span class="sxs-lookup"><span data-stu-id="1b36e-130">WH\_MSGFILTER and WH\_SYSMSGFILTER</span></span>](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [<span data-ttu-id="1b36e-131">WH \_ SHELL</span><span class="sxs-lookup"><span data-stu-id="1b36e-131">WH\_SHELL</span></span>](#wh_shell)

## <a name="hook-chains"></a><span data-ttu-id="1b36e-132">攔截鏈</span><span class="sxs-lookup"><span data-stu-id="1b36e-132">Hook Chains</span></span>

<span data-ttu-id="1b36e-133">系統支援許多不同類型的攔截;每個類型都可讓您存取其訊息處理機制的不同層面。</span><span class="sxs-lookup"><span data-stu-id="1b36e-133">The system supports many different types of hooks; each type provides access to a different aspect of its message-handling mechanism.</span></span> <span data-ttu-id="1b36e-134">例如，應用程式可以使用 WH 的 [ \_ 滑鼠](#wh_mouse) 掛勾來監視滑鼠訊息的訊息流量。</span><span class="sxs-lookup"><span data-stu-id="1b36e-134">For example, an application can use the [WH\_MOUSE](#wh_mouse) hook to monitor the message traffic for mouse messages.</span></span>

<span data-ttu-id="1b36e-135">系統會針對每一種類型的勾點維護個別的勾點。</span><span class="sxs-lookup"><span data-stu-id="1b36e-135">The system maintains a separate hook chain for each type of hook.</span></span> <span data-ttu-id="1b36e-136">攔截 *鏈* 是指向特殊應用程式定義回呼函式的指標清單，稱為攔截 *程式*。</span><span class="sxs-lookup"><span data-stu-id="1b36e-136">A *hook chain* is a list of pointers to special, application-defined callback functions called *hook procedures*.</span></span> <span data-ttu-id="1b36e-137">當發生與特定類型之攔截相關聯的訊息時，系統會將該訊息傳遞給勾點中所參考的每個攔截程式，然後再一次。</span><span class="sxs-lookup"><span data-stu-id="1b36e-137">When a message occurs that is associated with a particular type of hook, the system passes the message to each hook procedure referenced in the hook chain, one after the other.</span></span> <span data-ttu-id="1b36e-138">攔截程式可以採取的動作取決於所涉及的掛勾類型。</span><span class="sxs-lookup"><span data-stu-id="1b36e-138">The action a hook procedure can take depends on the type of hook involved.</span></span> <span data-ttu-id="1b36e-139">某些攔截程式類型的攔截程式只能監視訊息;其他人可以修改訊息或停止其進度，使其無法到達下一個勾點程式或目的地視窗。</span><span class="sxs-lookup"><span data-stu-id="1b36e-139">The hook procedures for some types of hooks can only monitor messages; others can modify messages or stop their progress through the chain, preventing them from reaching the next hook procedure or the destination window.</span></span>

## <a name="hook-procedures"></a><span data-ttu-id="1b36e-140">攔截程式</span><span class="sxs-lookup"><span data-stu-id="1b36e-140">Hook Procedures</span></span>

<span data-ttu-id="1b36e-141">為了充分利用特定類型的攔截程式，開發人員會提供攔截程式，並使用 [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) 函式將它安裝到與攔截相關聯的鏈中。</span><span class="sxs-lookup"><span data-stu-id="1b36e-141">To take advantage of a particular type of hook, the developer provides a hook procedure and uses the [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) function to install it into the chain associated with the hook.</span></span> <span data-ttu-id="1b36e-142">攔截程式必須有下列語法：</span><span class="sxs-lookup"><span data-stu-id="1b36e-142">A hook procedure must have the following syntax:</span></span>

``` syntax
LRESULT CALLBACK HookProc(
  int nCode, 
  WPARAM wParam, 
  LPARAM lParam
)
{
   // process event
   ...

   return CallNextHookEx(NULL, nCode, wParam, lParam);
}
```

<span data-ttu-id="1b36e-143">*HookProc* 是應用程式定義名稱的預留位置。</span><span class="sxs-lookup"><span data-stu-id="1b36e-143">*HookProc* is a placeholder for an application-defined name.</span></span>

<span data-ttu-id="1b36e-144">*NCode* 參數是攔截程式用來判斷要執行之動作的攔截程式碼。</span><span class="sxs-lookup"><span data-stu-id="1b36e-144">The *nCode* parameter is a hook code that the hook procedure uses to determine the action to perform.</span></span> <span data-ttu-id="1b36e-145">攔截程式碼的值取決於攔截的類型;每個類型都有自己的一組特性，也就是攔截碼。</span><span class="sxs-lookup"><span data-stu-id="1b36e-145">The value of the hook code depends on the type of the hook; each type has its own characteristic set of hook codes.</span></span> <span data-ttu-id="1b36e-146">*WParam* 和 *lParam* 參數的值取決於攔截程式碼，但它們通常包含已傳送或張貼之訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1b36e-146">The values of the *wParam* and *lParam* parameters depend on the hook code, but they typically contain information about a message that was sent or posted.</span></span>

<span data-ttu-id="1b36e-147">[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)函式一律會在攔截鏈的開頭安裝攔截程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-147">The [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) function always installs a hook procedure at the beginning of a hook chain.</span></span> <span data-ttu-id="1b36e-148">當特定類型的攔截器所監視的事件發生時，系統會在與攔截相關聯的掛勾鏈開頭呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-148">When an event occurs that is monitored by a particular type of hook, the system calls the procedure at the beginning of the hook chain associated with the hook.</span></span> <span data-ttu-id="1b36e-149">鏈中的每個攔截程式會決定是否要將事件傳遞到下一個程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-149">Each hook procedure in the chain determines whether to pass the event to the next procedure.</span></span> <span data-ttu-id="1b36e-150">攔截程式會藉由呼叫 [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) 函數，將事件傳遞至下一個程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-150">A hook procedure passes an event to the next procedure by calling the [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) function.</span></span>

<span data-ttu-id="1b36e-151">請注意，某些攔截程式類型的攔截程式只能監視訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-151">Note that the hook procedures for some types of hooks can only monitor messages.</span></span> <span data-ttu-id="1b36e-152">無論特定程式是否呼叫 [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex)，系統都會將訊息傳遞至每個攔截程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-152">the system passes messages to each hook procedure, regardless of whether a particular procedure calls [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="1b36e-153">*全域* 攔截會監視與呼叫執行緒位於相同桌面的所有線程的訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-153">A *global hook* monitors messages for all threads in the same desktop as the calling thread.</span></span> <span data-ttu-id="1b36e-154">*執行緒特定的勾* 點只會監視個別執行緒的訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-154">A *thread-specific hook* monitors messages for only an individual thread.</span></span> <span data-ttu-id="1b36e-155">全域攔截程式可以在與呼叫執行緒相同的桌面的任何應用程式內容中呼叫，因此程式必須位於不同的 DLL 模組中。</span><span class="sxs-lookup"><span data-stu-id="1b36e-155">A global hook procedure can be called in the context of any application in the same desktop as the calling thread, so the procedure must be in a separate DLL module.</span></span> <span data-ttu-id="1b36e-156">只有在相關聯的執行緒內容中，才會呼叫執行緒特定的勾點程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-156">A thread-specific hook procedure is called only in the context of the associated thread.</span></span> <span data-ttu-id="1b36e-157">如果應用程式為它自己的其中一個執行緒安裝攔截程式，則攔截程式可以是與應用程式的其餘部分程式碼或 DLL 中的其他程式碼相同的模組。</span><span class="sxs-lookup"><span data-stu-id="1b36e-157">If an application installs a hook procedure for one of its own threads, the hook procedure can be in either the same module as the rest of the application's code or in a DLL.</span></span> <span data-ttu-id="1b36e-158">如果應用程式針對不同應用程式的執行緒安裝攔截程式，則程式必須位於 DLL 中。</span><span class="sxs-lookup"><span data-stu-id="1b36e-158">If the application installs a hook procedure for a thread of a different application, the procedure must be in a DLL.</span></span> <span data-ttu-id="1b36e-159">如需詳細資訊，請參閱 [動態連結程式庫](../dlls/dynamic-link-libraries.md)。</span><span class="sxs-lookup"><span data-stu-id="1b36e-159">For information, see [Dynamic-Link Libraries](../dlls/dynamic-link-libraries.md).</span></span>

> [!Note]  
> <span data-ttu-id="1b36e-160">您應該只針對進行調試時使用全域攔截;否則，您應該避免這些問題。</span><span class="sxs-lookup"><span data-stu-id="1b36e-160">You should use global hooks only for debugging purposes; otherwise, you should avoid them.</span></span> <span data-ttu-id="1b36e-161">全域勾點會危害系統效能，並與其他可執行相同類型之全域攔截的應用程式產生衝突。</span><span class="sxs-lookup"><span data-stu-id="1b36e-161">Global hooks hurt system performance and cause conflicts with other applications that implement the same type of global hook.</span></span>

 

## <a name="hook-types"></a><span data-ttu-id="1b36e-162">掛勾類型</span><span class="sxs-lookup"><span data-stu-id="1b36e-162">Hook Types</span></span>

<span data-ttu-id="1b36e-163">每種類型的勾點都可讓應用程式監視系統訊息處理機制的不同層面。</span><span class="sxs-lookup"><span data-stu-id="1b36e-163">Each type of hook enables an application to monitor a different aspect of the system's message-handling mechanism.</span></span> <span data-ttu-id="1b36e-164">下列各節說明可用的勾點。</span><span class="sxs-lookup"><span data-stu-id="1b36e-164">The following sections describe the available hooks.</span></span>

-   [<span data-ttu-id="1b36e-165">WH \_ CALLWNDPROC 和 WH \_ CALLWNDPROCRET</span><span class="sxs-lookup"><span data-stu-id="1b36e-165">WH\_CALLWNDPROC and WH\_CALLWNDPROCRET</span></span>](#wh_callwndproc-and-wh_callwndprocret)
-   [<span data-ttu-id="1b36e-166">WH \_ CBT</span><span class="sxs-lookup"><span data-stu-id="1b36e-166">WH\_CBT</span></span>](#wh_cbt)
-   [<span data-ttu-id="1b36e-167">WH \_ DEBUG</span><span class="sxs-lookup"><span data-stu-id="1b36e-167">WH\_DEBUG</span></span>](#wh_debug)
-   [<span data-ttu-id="1b36e-168">WH \_ FOREGROUNDIDLE</span><span class="sxs-lookup"><span data-stu-id="1b36e-168">WH\_FOREGROUNDIDLE</span></span>](#wh_foregroundidle)
-   [<span data-ttu-id="1b36e-169">WH \_ GETMESSAGE</span><span class="sxs-lookup"><span data-stu-id="1b36e-169">WH\_GETMESSAGE</span></span>](#wh_getmessage)
-   [<span data-ttu-id="1b36e-170">WH \_ JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="1b36e-170">WH\_JOURNALPLAYBACK</span></span>](#wh_journalplayback)
-   [<span data-ttu-id="1b36e-171">WH \_ JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="1b36e-171">WH\_JOURNALRECORD</span></span>](#wh_journalrecord)
-   [<span data-ttu-id="1b36e-172">WH \_ 鍵盤 \_ LL</span><span class="sxs-lookup"><span data-stu-id="1b36e-172">WH\_KEYBOARD\_LL</span></span>](#wh_keyboard_ll)
-   [<span data-ttu-id="1b36e-173">WH \_ 鍵盤</span><span class="sxs-lookup"><span data-stu-id="1b36e-173">WH\_KEYBOARD</span></span>](#wh_keyboard)
-   [<span data-ttu-id="1b36e-174">WH \_ 滑鼠 \_ LL</span><span class="sxs-lookup"><span data-stu-id="1b36e-174">WH\_MOUSE\_LL</span></span>](#wh_mouse_ll)
-   [<span data-ttu-id="1b36e-175">WH \_ 滑鼠</span><span class="sxs-lookup"><span data-stu-id="1b36e-175">WH\_MOUSE</span></span>](#wh_mouse)
-   [<span data-ttu-id="1b36e-176">WH \_ MSGFILTER 和 WH \_ SYSMSGFILTER</span><span class="sxs-lookup"><span data-stu-id="1b36e-176">WH\_MSGFILTER and WH\_SYSMSGFILTER</span></span>](#wh_msgfilter-and-wh_sysmsgfilter)
-   [<span data-ttu-id="1b36e-177">WH \_ SHELL</span><span class="sxs-lookup"><span data-stu-id="1b36e-177">WH\_SHELL</span></span>](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a><span data-ttu-id="1b36e-178">WH \_ CALLWNDPROC 和 WH \_ CALLWNDPROCRET</span><span class="sxs-lookup"><span data-stu-id="1b36e-178">WH\_CALLWNDPROC and WH\_CALLWNDPROCRET</span></span>

<span data-ttu-id="1b36e-179">**WH \_ CALLWNDPROC** 和 **WH \_ CALLWNDPROCRET** 勾點可讓您監視傳送至視窗程式的訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-179">The **WH\_CALLWNDPROC** and **WH\_CALLWNDPROCRET** hooks enable you to monitor messages sent to window procedures.</span></span> <span data-ttu-id="1b36e-180">系統會先呼叫 **WH \_ CALLWNDPROC** 攔截程式，再將訊息傳遞至接收視窗程式，並在視窗程式處理訊息之後呼叫 **WH \_ CALLWNDPROCRET** 攔截程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-180">The system calls a **WH\_CALLWNDPROC** hook procedure before passing the message to the receiving window procedure, and calls the **WH\_CALLWNDPROCRET** hook procedure after the window procedure has processed the message.</span></span>

<span data-ttu-id="1b36e-181">**WH \_ CALLWNDPROCRET** 勾點會將 [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct)結構的指標傳遞至攔截程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-181">The **WH\_CALLWNDPROCRET** hook passes a pointer to a [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) structure to the hook procedure.</span></span> <span data-ttu-id="1b36e-182">結構包含處理訊息之視窗程式的傳回值，以及與訊息相關聯的訊息參數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-182">The structure contains the return value from the window procedure that processed the message, as well as the message parameters associated with the message.</span></span> <span data-ttu-id="1b36e-183">子類別化視窗不適用於在進程間設定的訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-183">Subclassing the window does not work for messages set between processes.</span></span>

<span data-ttu-id="1b36e-184">如需詳細資訊，請參閱 [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) 和 [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-184">For more information, see the [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) and [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc) callback functions.</span></span>

### <a name="wh_cbt"></a><span data-ttu-id="1b36e-185">WH \_ CBT</span><span class="sxs-lookup"><span data-stu-id="1b36e-185">WH\_CBT</span></span>

<span data-ttu-id="1b36e-186">系統會先呼叫 **WH 的 \_ CBT** 攔截程式，然後再啟用、建立、終結、最小化、最大化、移動或調整視窗大小、完成系統命令之前，先從系統訊息佇列移除滑鼠或鍵盤事件，然後再設定輸入焦點，或在與系統訊息佇列進行同步處理之前。</span><span class="sxs-lookup"><span data-stu-id="1b36e-186">The system calls a **WH\_CBT** hook procedure before activating, creating, destroying, minimizing, maximizing, moving, or sizing a window; before completing a system command; before removing a mouse or keyboard event from the system message queue; before setting the input focus; or before synchronizing with the system message queue.</span></span> <span data-ttu-id="1b36e-187">攔截程式傳回的值會決定系統是否允許或防止其中一項作業。</span><span class="sxs-lookup"><span data-stu-id="1b36e-187">The value the hook procedure returns determines whether the system allows or prevents one of these operations.</span></span> <span data-ttu-id="1b36e-188">**WH 的 \_ cbt** 攔截主要用於以電腦為基礎的訓練 (CBT) 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-188">The **WH\_CBT** hook is intended primarily for computer-based training (CBT) applications.</span></span>

<span data-ttu-id="1b36e-189">如需詳細資訊，請參閱 [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-189">For more information, see the [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) callback function.</span></span>

<span data-ttu-id="1b36e-190">如需詳細資訊，請參閱 [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure)。</span><span class="sxs-lookup"><span data-stu-id="1b36e-190">For information, see [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).</span></span>

### <a name="wh_debug"></a><span data-ttu-id="1b36e-191">WH \_ DEBUG</span><span class="sxs-lookup"><span data-stu-id="1b36e-191">WH\_DEBUG</span></span>

<span data-ttu-id="1b36e-192">系統會先呼叫 **WH \_** 的偵測攔截程式，再呼叫與系統中任何其他連結相關聯的勾點程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-192">The system calls a **WH\_DEBUG** hook procedure before calling hook procedures associated with any other hook in the system.</span></span> <span data-ttu-id="1b36e-193">您可以使用此攔截來判斷是否允許系統呼叫與其他類型之攔截相關聯的勾點程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-193">You can use this hook to determine whether to allow the system to call hook procedures associated with other types of hooks.</span></span>

<span data-ttu-id="1b36e-194">如需詳細資訊，請參閱 [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-194">For more information, see the [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) callback function.</span></span>

### <a name="wh_foregroundidle"></a><span data-ttu-id="1b36e-195">WH \_ FOREGROUNDIDLE</span><span class="sxs-lookup"><span data-stu-id="1b36e-195">WH\_FOREGROUNDIDLE</span></span>

<span data-ttu-id="1b36e-196">**WH \_ FOREGROUNDIDLE** 勾點可讓您在其前景執行緒閒置的期間，執行低優先順序的工作。</span><span class="sxs-lookup"><span data-stu-id="1b36e-196">The **WH\_FOREGROUNDIDLE** hook enables you to perform low priority tasks during times when its foreground thread is idle.</span></span> <span data-ttu-id="1b36e-197">當應用程式的前景執行緒即將閒置時，系統會呼叫 **WH \_ FOREGROUNDIDLE** 攔截程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-197">The system calls a **WH\_FOREGROUNDIDLE** hook procedure when the application's foreground thread is about to become idle.</span></span>

<span data-ttu-id="1b36e-198">如需詳細資訊，請參閱 [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-198">For more information, see the [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) callback function.</span></span>

### <a name="wh_getmessage"></a><span data-ttu-id="1b36e-199">WH \_ GETMESSAGE</span><span class="sxs-lookup"><span data-stu-id="1b36e-199">WH\_GETMESSAGE</span></span>

<span data-ttu-id="1b36e-200">**WH \_ GETMESSAGE** 攔截可讓應用程式監視有關 [**GETMESSAGE**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)函式所傳回的訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-200">The **WH\_GETMESSAGE** hook enables an application to monitor messages about to be returned by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <span data-ttu-id="1b36e-201">您可以使用 **WH \_ GETMESSAGE** 掛勾來監視滑鼠和鍵盤輸入，以及張貼至訊息佇列的其他訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-201">You can use the **WH\_GETMESSAGE** hook to monitor mouse and keyboard input and other messages posted to the message queue.</span></span>

<span data-ttu-id="1b36e-202">如需詳細資訊，請參閱 [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-202">For more information, see the [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function.</span></span>

### <a name="wh_journalplayback"></a><span data-ttu-id="1b36e-203">WH \_ JOURNALPLAYBACK</span><span class="sxs-lookup"><span data-stu-id="1b36e-203">WH\_JOURNALPLAYBACK</span></span>

<span data-ttu-id="1b36e-204">**WH \_ JOURNALPLAYBACK** 攔截可讓應用程式將訊息插入系統訊息佇列。</span><span class="sxs-lookup"><span data-stu-id="1b36e-204">The **WH\_JOURNALPLAYBACK** hook enables an application to insert messages into the system message queue.</span></span> <span data-ttu-id="1b36e-205">您可以使用此攔截來播放先前使用 [WH \_ JOURNALRECORD](#wh_journalrecord)錄製的一系列滑鼠和鍵盤事件。</span><span class="sxs-lookup"><span data-stu-id="1b36e-205">You can use this hook to play back a series of mouse and keyboard events recorded earlier by using [WH\_JOURNALRECORD](#wh_journalrecord).</span></span> <span data-ttu-id="1b36e-206">只要安裝了 **WH \_ JOURNALPLAYBACK** 勾點，就會停用一般滑鼠和鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="1b36e-206">Regular mouse and keyboard input is disabled as long as a **WH\_JOURNALPLAYBACK** hook is installed.</span></span> <span data-ttu-id="1b36e-207">**WH \_ JOURNALPLAYBACK** 攔截是一種全域攔截，不能用來做為執行緒特定的勾點。</span><span class="sxs-lookup"><span data-stu-id="1b36e-207">A **WH\_JOURNALPLAYBACK** hook is a global hook—it cannot be used as a thread-specific hook.</span></span>

<span data-ttu-id="1b36e-208">**WH \_ JOURNALPLAYBACK** 勾點會傳回超時值。</span><span class="sxs-lookup"><span data-stu-id="1b36e-208">The **WH\_JOURNALPLAYBACK** hook returns a time-out value.</span></span> <span data-ttu-id="1b36e-209">此值會告訴系統在處理來自播放攔截的目前訊息之前，要等待的毫秒數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-209">This value tells the system how many milliseconds to wait before processing the current message from the playback hook.</span></span> <span data-ttu-id="1b36e-210">這可讓攔截控制其播放事件的時間。</span><span class="sxs-lookup"><span data-stu-id="1b36e-210">This enables the hook to control the timing of the events it plays back.</span></span>

<span data-ttu-id="1b36e-211">如需詳細資訊，請參閱 [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-211">For more information, see the [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) callback function.</span></span>

### <a name="wh_journalrecord"></a><span data-ttu-id="1b36e-212">WH \_ JOURNALRECORD</span><span class="sxs-lookup"><span data-stu-id="1b36e-212">WH\_JOURNALRECORD</span></span>

<span data-ttu-id="1b36e-213">**WH \_ JOURNALRECORD** 勾點可讓您監視和記錄輸入事件。</span><span class="sxs-lookup"><span data-stu-id="1b36e-213">The **WH\_JOURNALRECORD** hook enables you to monitor and record input events.</span></span> <span data-ttu-id="1b36e-214">一般來說，您會使用這個攔截來記錄一系列的滑鼠和鍵盤事件，稍後再使用 [WH \_ JOURNALPLAYBACK](#wh_journalplayback)播放。</span><span class="sxs-lookup"><span data-stu-id="1b36e-214">Typically, you use this hook to record a sequence of mouse and keyboard events to play back later by using [WH\_JOURNALPLAYBACK](#wh_journalplayback).</span></span> <span data-ttu-id="1b36e-215">**WH \_ JOURNALRECORD** 攔截是一種全域攔截，不能用來做為執行緒特定的勾點。</span><span class="sxs-lookup"><span data-stu-id="1b36e-215">The **WH\_JOURNALRECORD** hook is a global hook—it cannot be used as a thread-specific hook.</span></span>

<span data-ttu-id="1b36e-216">如需詳細資訊，請參閱 [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-216">For more information, see the [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) callback function.</span></span>

### <a name="wh_keyboard_ll"></a><span data-ttu-id="1b36e-217">WH \_ 鍵盤 \_ LL</span><span class="sxs-lookup"><span data-stu-id="1b36e-217">WH\_KEYBOARD\_LL</span></span>

<span data-ttu-id="1b36e-218">**WH \_ 鍵盤 \_** 串連可讓您監視要張貼線上程輸入佇列中的鍵盤輸入事件。</span><span class="sxs-lookup"><span data-stu-id="1b36e-218">The **WH\_KEYBOARD\_LL** hook enables you to monitor keyboard input events about to be posted in a thread input queue.</span></span>

<span data-ttu-id="1b36e-219">如需詳細資訊，請參閱 [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-219">For more information, see the [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) callback function.</span></span>

### <a name="wh_keyboard"></a><span data-ttu-id="1b36e-220">WH \_ 鍵盤</span><span class="sxs-lookup"><span data-stu-id="1b36e-220">WH\_KEYBOARD</span></span>

<span data-ttu-id="1b36e-221">**WH \_ 鍵盤** 勾點可讓應用程式監視有關 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)函式所傳回之 [**wm \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown)和 [**wm \_ KEYUP**](/windows/desktop/inputdev/wm-keyup)訊息的訊息流量。</span><span class="sxs-lookup"><span data-stu-id="1b36e-221">The **WH\_KEYBOARD** hook enables an application to monitor message traffic for [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) and [**WM\_KEYUP**](/windows/desktop/inputdev/wm-keyup) messages about to be returned by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <span data-ttu-id="1b36e-222">您可以使用 **WH \_ 鍵盤** 掛勾來監視張貼至訊息佇列的鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="1b36e-222">You can use the **WH\_KEYBOARD** hook to monitor keyboard input posted to a message queue.</span></span>

<span data-ttu-id="1b36e-223">如需詳細資訊，請參閱 [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-223">For more information, see the [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) callback function.</span></span>

### <a name="wh_mouse_ll"></a><span data-ttu-id="1b36e-224">WH \_ 滑鼠 \_ LL</span><span class="sxs-lookup"><span data-stu-id="1b36e-224">WH\_MOUSE\_LL</span></span>

<span data-ttu-id="1b36e-225">**WH 的 \_ 滑鼠 \_ LL** 可讓您監視要張貼線上程輸入佇列中的滑鼠輸入事件。</span><span class="sxs-lookup"><span data-stu-id="1b36e-225">The **WH\_MOUSE\_LL** hook enables you to monitor mouse input events about to be posted in a thread input queue.</span></span>

<span data-ttu-id="1b36e-226">如需詳細資訊，請參閱 [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-226">For more information, see the [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) callback function.</span></span>

### <a name="wh_mouse"></a><span data-ttu-id="1b36e-227">WH \_ 滑鼠</span><span class="sxs-lookup"><span data-stu-id="1b36e-227">WH\_MOUSE</span></span>

<span data-ttu-id="1b36e-228">**WH 的 \_ 滑鼠** 勾點可讓您監視有關 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)或 [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)函式要傳回的滑鼠訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-228">The **WH\_MOUSE** hook enables you to monitor mouse messages about to be returned by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <span data-ttu-id="1b36e-229">您可以使用 **WH \_ 滑鼠** 掛勾來監視張貼到訊息佇列的滑鼠輸入。</span><span class="sxs-lookup"><span data-stu-id="1b36e-229">You can use the **WH\_MOUSE** hook to monitor mouse input posted to a message queue.</span></span>

<span data-ttu-id="1b36e-230">如需詳細資訊，請參閱 [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-230">For more information, see the [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) callback function.</span></span>

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a><span data-ttu-id="1b36e-231">WH \_ MSGFILTER 和 WH \_ SYSMSGFILTER</span><span class="sxs-lookup"><span data-stu-id="1b36e-231">WH\_MSGFILTER and WH\_SYSMSGFILTER</span></span>

<span data-ttu-id="1b36e-232">**WH \_ MSGFILTER** 和 **WH \_ SYSMSGFILTER** 勾點可讓您監視要由功能表、捲軸、訊息方塊或對話方塊處理的訊息，以及偵測當使用者按下 ALT + tab 或 ALT + ESC 鍵組合時，何時即將啟動不同的視窗。</span><span class="sxs-lookup"><span data-stu-id="1b36e-232">The **WH\_MSGFILTER** and **WH\_SYSMSGFILTER** hooks enable you to monitor messages about to be processed by a menu, scroll bar, message box, or dialog box, and to detect when a different window is about to be activated as a result of the user's pressing the ALT+TAB or ALT+ESC key combination.</span></span> <span data-ttu-id="1b36e-233">**WH \_ MSGFILTER** 攔截只能監視傳遞至已安裝攔截程式之應用程式所建立之功能表、捲軸、訊息方塊或對話方塊的訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-233">The **WH\_MSGFILTER** hook can only monitor messages passed to a menu, scroll bar, message box, or dialog box created by the application that installed the hook procedure.</span></span> <span data-ttu-id="1b36e-234">**WH \_ SYSMSGFILTER** 攔截會監視所有應用程式的這類訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-234">The **WH\_SYSMSGFILTER** hook monitors such messages for all applications.</span></span>

<span data-ttu-id="1b36e-235">**WH \_ MSGFILTER** 和 **WH \_ SYSMSGFILTER** 勾點可讓您在強制回應迴圈期間執行訊息篩選，這相當於在主要訊息迴圈中完成的篩選。</span><span class="sxs-lookup"><span data-stu-id="1b36e-235">The **WH\_MSGFILTER** and **WH\_SYSMSGFILTER** hooks enable you to perform message filtering during modal loops that is equivalent to the filtering done in the main message loop.</span></span> <span data-ttu-id="1b36e-236">例如，應用程式通常會在從佇列中取得訊息的時間和分派訊息的時間之間，檢查主迴圈中的新訊息，並適當地執行特殊處理。</span><span class="sxs-lookup"><span data-stu-id="1b36e-236">For example, an application often examines a new message in the main loop between the time it retrieves the message from the queue and the time it dispatches the message, performing special processing as appropriate.</span></span> <span data-ttu-id="1b36e-237">不過，在強制回應迴圈期間，系統會在不允許應用程式在其主要訊息迴圈中篩選訊息的機會下，抓取並分派訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-237">However, during a modal loop, the system retrieves and dispatches messages without allowing an application the chance to filter the messages in its main message loop.</span></span> <span data-ttu-id="1b36e-238">如果應用程式安裝 **WH \_ MSGFILTER** 或 **WH \_ SYSMSGFILTER** 攔截程式，系統會在強制回應迴圈期間呼叫程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-238">If an application installs a **WH\_MSGFILTER** or **WH\_SYSMSGFILTER** hook procedure, the system calls the procedure during the modal loop.</span></span>

<span data-ttu-id="1b36e-239">應用程式可以藉由呼叫 [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera)函式，直接呼叫 **WH \_ MSGFILTER** 掛勾。</span><span class="sxs-lookup"><span data-stu-id="1b36e-239">An application can call the **WH\_MSGFILTER** hook directly by calling the [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) function.</span></span> <span data-ttu-id="1b36e-240">藉由使用這個函數，應用程式可以使用相同的程式碼在強制回應迴圈期間篩選訊息，因為它在主要訊息迴圈中使用。</span><span class="sxs-lookup"><span data-stu-id="1b36e-240">By using this function, the application can use the same code to filter messages during modal loops as it uses in the main message loop.</span></span> <span data-ttu-id="1b36e-241">若要這樣做，請在 **WH \_ MSGFILTER** 攔截程式中封裝篩選作業，並在 [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)和 [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)函數的呼叫之間呼叫 **CallMsgFilter** 。</span><span class="sxs-lookup"><span data-stu-id="1b36e-241">To do so, encapsulate the filtering operations in a **WH\_MSGFILTER** hook procedure and call **CallMsgFilter** between the calls to the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) and [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) functions.</span></span>

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

<span data-ttu-id="1b36e-242">[**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera)的最後一個引數會直接傳遞至攔截程式;您可以輸入任何值。</span><span class="sxs-lookup"><span data-stu-id="1b36e-242">The last argument of [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) is simply passed to the hook procedure; you can enter any value.</span></span> <span data-ttu-id="1b36e-243">藉由定義常數（例如 **MSGF \_ MAINLOOP**），攔截程式就可以使用此值來判斷呼叫程式的位置。</span><span class="sxs-lookup"><span data-stu-id="1b36e-243">The hook procedure, by defining a constant such as **MSGF\_MAINLOOP**, can use this value to determine where the procedure was called from.</span></span>

<span data-ttu-id="1b36e-244">如需詳細資訊，請參閱 [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) 和 [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-244">For more information, see the [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) and [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) callback functions.</span></span>

### <a name="wh_shell"></a><span data-ttu-id="1b36e-245">WH \_ SHELL</span><span class="sxs-lookup"><span data-stu-id="1b36e-245">WH\_SHELL</span></span>

<span data-ttu-id="1b36e-246">Shell 應用程式可以使用 **WH \_ shell** 攔截來接收重要通知。</span><span class="sxs-lookup"><span data-stu-id="1b36e-246">A shell application can use the **WH\_SHELL** hook to receive important notifications.</span></span> <span data-ttu-id="1b36e-247">當 SHELL 應用程式即將啟動，以及建立或終結最上層視窗時，系統會呼叫 **WH \_ shell** 攔截程式。</span><span class="sxs-lookup"><span data-stu-id="1b36e-247">The system calls a **WH\_SHELL** hook procedure when the shell application is about to be activated and when a top-level window is created or destroyed.</span></span>

<span data-ttu-id="1b36e-248">請注意，自訂 shell 應用程式不會接收 **WH \_ shell** 訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-248">Note that custom shell applications do not receive **WH\_SHELL** messages.</span></span> <span data-ttu-id="1b36e-249">因此，將本身註冊為預設 shell 的任何應用程式，都必須在 (之前呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函式，或任何其他應用程式) 可以接收 **WH \_ shell** 訊息。</span><span class="sxs-lookup"><span data-stu-id="1b36e-249">Therefore, any application that registers itself as the default shell must call the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function before it (or any other application) can receive **WH\_SHELL** messages.</span></span> <span data-ttu-id="1b36e-250">您必須使用 **SPI \_ SETMINIMIZEDMETRICS** 和 [**MINIMIZEDMETRICS**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) 結構來呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-250">This function must be called with **SPI\_SETMINIMIZEDMETRICS** and a [**MINIMIZEDMETRICS**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) structure.</span></span> <span data-ttu-id="1b36e-251">將此結構的 **iArrange** 成員設定為 **ARW \_ HIDE**。</span><span class="sxs-lookup"><span data-stu-id="1b36e-251">Set the **iArrange** member of this structure to **ARW\_HIDE**.</span></span>

<span data-ttu-id="1b36e-252">如需詳細資訊，請參閱 [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) 回呼函數。</span><span class="sxs-lookup"><span data-stu-id="1b36e-252">For more information, see the [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) callback function.</span></span>

 

 
