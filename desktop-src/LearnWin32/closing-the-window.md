---
title: 關閉視窗
description: 當使用者關閉視窗時，該動作就會觸發一連串的視窗訊息。
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842304"
---
# <a name="closing-the-window"></a><span data-ttu-id="05e19-103">關閉視窗</span><span class="sxs-lookup"><span data-stu-id="05e19-103">Closing the Window</span></span>

<span data-ttu-id="05e19-104">當使用者關閉視窗時，該動作就會觸發一連串的視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="05e19-104">When the user closes a window, that action triggers a sequence of window messages.</span></span>

<span data-ttu-id="05e19-105">使用者可以按一下 [ **關閉** ] 按鈕，或使用鍵盤快速鍵（例如 ALT + F4）關閉應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="05e19-105">The user can close an application window by clicking the **Close** button, or by using a keyboard shortcut such as ALT+F4.</span></span> <span data-ttu-id="05e19-106">其中任何一項動作都會導致視窗收到 [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close) 訊息。</span><span class="sxs-lookup"><span data-stu-id="05e19-106">Any of these actions causes the window to receive a [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) message.</span></span> <span data-ttu-id="05e19-107">**WM \_ 關閉** 訊息讓您有機會在關閉視窗之前提示使用者。</span><span class="sxs-lookup"><span data-stu-id="05e19-107">The **WM\_CLOSE** message gives you an opportunity to prompt the user before closing the window.</span></span> <span data-ttu-id="05e19-108">如果您真的想要關閉視窗，請呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) 函數。</span><span class="sxs-lookup"><span data-stu-id="05e19-108">If you really do want to close the window, call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function.</span></span> <span data-ttu-id="05e19-109">否則，只會從 **WM \_ 關閉** 訊息傳回零，而且作業系統會忽略該訊息，而不會損毀視窗。</span><span class="sxs-lookup"><span data-stu-id="05e19-109">Otherwise, simply return zero from the **WM\_CLOSE** message, and the operating system will ignore the message and not destroy the window.</span></span>

<span data-ttu-id="05e19-110">以下是程式可能處理 [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close)的範例。</span><span class="sxs-lookup"><span data-stu-id="05e19-110">Here is an example of how a program might handle [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span>

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

<span data-ttu-id="05e19-111">在此範例中， [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) 函式會顯示模式對話方塊，其中包含 **[確定** ] 和 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="05e19-111">In this example, the [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) function shows a modal dialog that contains **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="05e19-112">如果使用者按一下 **[確定]**，程式就會呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow)。</span><span class="sxs-lookup"><span data-stu-id="05e19-112">If the user clicks **OK**, the program calls [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span></span> <span data-ttu-id="05e19-113">否則，如果使用者按一下 [ **取消**]，則會略過對 **DestroyWindow** 的呼叫，且視窗會保持開啟狀態。</span><span class="sxs-lookup"><span data-stu-id="05e19-113">Otherwise, if the user clicks **Cancel**, the call to **DestroyWindow** is skipped, and the window remains open.</span></span> <span data-ttu-id="05e19-114">在任一種情況下，都會傳回零以表示您已處理訊息。</span><span class="sxs-lookup"><span data-stu-id="05e19-114">In either case, return zero to indicate that you handled the message.</span></span>

<span data-ttu-id="05e19-115">如果您想要關閉視窗而不提示使用者，您可以直接呼叫 [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) ，而不需要呼叫 [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox)。</span><span class="sxs-lookup"><span data-stu-id="05e19-115">If you want to close the window without prompting the user, you could simply call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) without the call to [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span></span> <span data-ttu-id="05e19-116">不過，在此情況下有一個快捷方式。</span><span class="sxs-lookup"><span data-stu-id="05e19-116">However, there is a shortcut in this case.</span></span> <span data-ttu-id="05e19-117">回想一下， [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 會執行任何視窗訊息的預設動作。</span><span class="sxs-lookup"><span data-stu-id="05e19-117">Recall that [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executes the default action for any window message.</span></span> <span data-ttu-id="05e19-118">在 [**WM \_ 關閉**](/windows/desktop/winmsg/wm-close)的情況下， **DefWindowProc** 會自動呼叫 **DestroyWindow**。</span><span class="sxs-lookup"><span data-stu-id="05e19-118">In the case of [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), **DefWindowProc** automatically calls **DestroyWindow**.</span></span> <span data-ttu-id="05e19-119">這表示，如果您在 **switch** 語句中忽略 **WM \_ 關閉** 訊息，則預設會終結視窗。</span><span class="sxs-lookup"><span data-stu-id="05e19-119">That means if you ignore the **WM\_CLOSE** message in your **switch** statement, the window is destroyed by default.</span></span>

<span data-ttu-id="05e19-120">當視窗即將終結時，它會收到 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy) 訊息。</span><span class="sxs-lookup"><span data-stu-id="05e19-120">When a window is about to be destroyed, it receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="05e19-121">這則訊息會在視窗從螢幕中移除之後傳送，但在銷毀之前 (特別是在) 之前終結任何子視窗之前。</span><span class="sxs-lookup"><span data-stu-id="05e19-121">This message is sent after the window is removed from the screen, but before the destruction occurs (in particular, before any child windows are destroyed).</span></span>

<span data-ttu-id="05e19-122">在主應用程式視窗中，您通常會藉由呼叫 [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage)來回應 [**WM 損 \_ 毀**](/windows/desktop/winmsg/wm-destroy)。</span><span class="sxs-lookup"><span data-stu-id="05e19-122">In your main application window, you will typically respond to [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) by calling [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span>

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

<span data-ttu-id="05e19-123">在 [ [視窗訊息]](window-messages.md) 區段中， [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) 會在訊息佇列上放置一個 [**WM \_**](/windows/desktop/winmsg/wm-quit) 結束訊息，造成訊息迴圈結束。</span><span class="sxs-lookup"><span data-stu-id="05e19-123">We saw in the [Window Messages](window-messages.md) section that [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue, causing the message loop to end.</span></span>

<span data-ttu-id="05e19-124">以下流程圖顯示處理 [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close) 和 [**WM \_ 摧毀**](/windows/desktop/winmsg/wm-destroy) 訊息的一般方式：</span><span class="sxs-lookup"><span data-stu-id="05e19-124">Here is a flow chart showing the typical way to process [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) messages:</span></span>

![顯示如何處理 wm \- 關閉和 wm 損 \- 毀訊息的流程圖](images/wmclose01.png)

## <a name="next"></a><span data-ttu-id="05e19-126">下一個</span><span class="sxs-lookup"><span data-stu-id="05e19-126">Next</span></span>

[<span data-ttu-id="05e19-127">管理應用程式狀態</span><span class="sxs-lookup"><span data-stu-id="05e19-127">Managing Application State</span></span>](managing-application-state-.md)