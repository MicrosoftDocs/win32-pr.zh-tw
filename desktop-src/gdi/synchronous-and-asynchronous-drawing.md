---
description: 大部分在處理 WM 油漆訊息期間所執行的繪圖 \_ 都是非同步，也就是說，時間範圍的某個部分會失效，且傳送的時間為 WM 繪製的時間之間會有延遲 \_ 。
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: 同步和非同步繪圖
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945088"
---
# <a name="synchronous-and-asynchronous-drawing"></a><span data-ttu-id="090ac-103">同步和非同步繪圖</span><span class="sxs-lookup"><span data-stu-id="090ac-103">Synchronous and Asynchronous Drawing</span></span>

<span data-ttu-id="090ac-104">大部分在處理 [**WM \_ 油漆**](wm-paint.md) 訊息期間所執行的繪圖都是非同步，也就是說，時間範圍的某個部分會失效，且傳送的時間為 WM 繪製的時間之間會有延遲 \_ 。</span><span class="sxs-lookup"><span data-stu-id="090ac-104">Most drawing carried out during processing of the [**WM\_PAINT**](wm-paint.md) message is asynchronous; that is, there is a delay between the time a portion of the window is invalidated and the time WM\_PAINT is sent.</span></span> <span data-ttu-id="090ac-105">在延遲期間，應用程式通常會從佇列中取出訊息，並執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="090ac-105">During the delay, the application typically retrieves messages from the queue and carries out other tasks.</span></span> <span data-ttu-id="090ac-106">延遲的原因是系統通常會將視窗中的繪圖視為低優先順序作業，而且可以像使用者輸入訊息以及可能影響視窗的位置或大小的訊息，在 WM 油漆之前處理 \_ 。</span><span class="sxs-lookup"><span data-stu-id="090ac-106">The reason for the delay is that the system generally treats drawing in a window as a low-priority operation and works as though user-input messages and messages that may affect the position or size of a window will be processed before WM\_PAINT .</span></span>

<span data-ttu-id="090ac-107">在某些情況下，應用程式必須以同步方式繪製，也就是在視窗的某個部分之後立即在視窗中繪製。</span><span class="sxs-lookup"><span data-stu-id="090ac-107">In some cases, it is necessary for an application to draw synchronously that is, draw in the window immediately after invalidating a portion of the window.</span></span> <span data-ttu-id="090ac-108">一般的應用程式會在建立視窗後立即繪製其主視窗，以通知使用者應用程式已順利啟動。</span><span class="sxs-lookup"><span data-stu-id="090ac-108">A typical application draws its main window immediately after creating the window to signal the user that the application has started successfully.</span></span> <span data-ttu-id="090ac-109">系統會以同步的方式（例如按鈕）來繪製一些控制項視窗，因為這類 windows 可作為使用者輸入的焦點。</span><span class="sxs-lookup"><span data-stu-id="090ac-109">The system draws some control windows synchronously, such as buttons, because such windows serve as the focus for user input.</span></span> <span data-ttu-id="090ac-110">雖然可以同步繪製具有簡單繪圖常式的任何視窗，但是所有這類繪圖都應該快速完成，而且不會干擾應用程式回應使用者輸入的能力。</span><span class="sxs-lookup"><span data-stu-id="090ac-110">Although any window with a simple drawing routine can be drawn synchronously, all such drawing should be done quickly and should not interfere with the application's ability to respond to user input.</span></span>

<span data-ttu-id="090ac-111">[**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)和 [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)函式允許同步繪製。</span><span class="sxs-lookup"><span data-stu-id="090ac-111">The [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) and [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) functions allow for synchronous drawing.</span></span> <span data-ttu-id="090ac-112">如果更新區域不是空的， **UpdateWindow** 會直接將 [**WM \_ 油漆**](wm-paint.md)訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="090ac-112">**UpdateWindow** sends a [**WM\_PAINT**](wm-paint.md) message directly to the window if the update region is not empty.</span></span> <span data-ttu-id="090ac-113">**RedrawWindow** 也會傳送 **WM \_ 油漆** 訊息，但讓應用程式更能控制視窗的繪製方式，例如是否要繪製非工作區和視窗背景，或者是否要傳送訊息，而不論更新區域是否為空白。</span><span class="sxs-lookup"><span data-stu-id="090ac-113">**RedrawWindow** also sends a **WM\_PAINT** message, but gives the application greater control over how to draw the window, such as whether to draw the nonclient area and window background or whether to send the message regardless of whether the update region is empty.</span></span> <span data-ttu-id="090ac-114">無論應用程式訊息佇列中的其他訊息數目為何，這些函式都會直接將 **WM \_ 油漆** 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="090ac-114">These functions send the **WM\_PAINT** message directly to the window, regardless of the number of other messages in the application message queue.</span></span>

<span data-ttu-id="090ac-115">任何需要耗用耗時繪圖作業的視窗，都應該以非同步方式繪製，以防止在繪製視窗時封鎖暫止的訊息。</span><span class="sxs-lookup"><span data-stu-id="090ac-115">Any window requiring time-consuming drawing operations should be drawn asynchronously to prevent pending messages from being blocked as the window is drawn.</span></span> <span data-ttu-id="090ac-116">此外，任何經常使視窗的小部分失效的應用程式，都應該允許這些不正確部分合併到單一非同步 [**wm \_ 油漆**](wm-paint.md) 訊息中，而不是一系列的同步 **wm \_ 繪製** 訊息。</span><span class="sxs-lookup"><span data-stu-id="090ac-116">Also, any application that frequently invalidates small portions of a window should allow these invalid portions to consolidate into a single asynchronous [**WM\_PAINT**](wm-paint.md) message, rather than a series of synchronous **WM\_PAINT** messages.</span></span>

 

 



