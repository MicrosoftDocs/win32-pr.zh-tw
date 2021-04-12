---
title: 設定游標影像
description: 設定游標影像
ms.assetid: FB223131-19AE-41DD-87DE-73992AE2A0CA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3bc993b7566dee1fa47bd2b53c270ad0e4f64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463033"
---
# <a name="setting-the-cursor-image"></a><span data-ttu-id="94f9b-103">設定游標影像</span><span class="sxs-lookup"><span data-stu-id="94f9b-103">Setting the Cursor Image</span></span>

<span data-ttu-id="94f9b-104">*游標* 是顯示滑鼠或其他指標裝置位置的小型影像。</span><span class="sxs-lookup"><span data-stu-id="94f9b-104">The *cursor* is the small image that shows the location of the mouse or other pointing device.</span></span> <span data-ttu-id="94f9b-105">許多應用程式會變更游標影像，以將意見反應提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="94f9b-105">Many applications change the cursor image to give feedback to the user.</span></span> <span data-ttu-id="94f9b-106">雖然並非必要，但它會在您的應用程式中增加很棒的波蘭文。</span><span class="sxs-lookup"><span data-stu-id="94f9b-106">Although it is not required, it adds a nice bit of polish to your application.</span></span>

<span data-ttu-id="94f9b-107">Windows 提供一組標準的資料指標映射，稱為 *系統資料指標*。</span><span class="sxs-lookup"><span data-stu-id="94f9b-107">Windows provides a set of standard cursor images, called *system cursors*.</span></span> <span data-ttu-id="94f9b-108">其中包括箭號、手形、I-橫樑、沙漏 (現在是旋轉圓形) 和其他。</span><span class="sxs-lookup"><span data-stu-id="94f9b-108">These include the arrow, the hand, the I-beam, the hourglass (which is now a spinning circle), and others.</span></span> <span data-ttu-id="94f9b-109">本節說明如何使用系統資料指標。</span><span class="sxs-lookup"><span data-stu-id="94f9b-109">This section describes how to use the system cursors.</span></span> <span data-ttu-id="94f9b-110">如需更先進的工作，例如建立自訂資料指標，請參閱資料 [指標](/windows/desktop/menurc/cursors)。</span><span class="sxs-lookup"><span data-stu-id="94f9b-110">For more advanced tasks, such as creating custom cursors, see [Cursors](/windows/desktop/menurc/cursors).</span></span>

<span data-ttu-id="94f9b-111">您可以藉由設定 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)或 [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa)結構的 **hCursor** 成員，將資料指標與視窗類別產生關聯。</span><span class="sxs-lookup"><span data-stu-id="94f9b-111">You can associate a cursor with a window class by setting the **hCursor** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) or [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) structure.</span></span> <span data-ttu-id="94f9b-112">否則，預設資料指標就是箭號。</span><span class="sxs-lookup"><span data-stu-id="94f9b-112">Otherwise, the default cursor is the arrow.</span></span> <span data-ttu-id="94f9b-113">當滑鼠移至視窗上方時，除非有另一個視窗已捕捉到滑鼠) ，否則視窗會收到 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息 (。</span><span class="sxs-lookup"><span data-stu-id="94f9b-113">When the mouse moves over a window, the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message (unless another window has captured the mouse).</span></span> <span data-ttu-id="94f9b-114">此時會發生下列其中一個事件：</span><span class="sxs-lookup"><span data-stu-id="94f9b-114">At this point, one of the following events occurs:</span></span>

-   <span data-ttu-id="94f9b-115">應用程式會設定資料指標，而視窗程式會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="94f9b-115">The application sets the cursor and the window procedure returns **TRUE**.</span></span>
-   <span data-ttu-id="94f9b-116">應用程式不會執行任何動作，並且會將 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)。</span><span class="sxs-lookup"><span data-stu-id="94f9b-116">The application does nothing and passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="94f9b-117">若要設定資料指標，程式會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="94f9b-117">To set the cursor, a program does the following:</span></span>

1.  <span data-ttu-id="94f9b-118">呼叫 [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) 將資料指標載入記憶體中。</span><span class="sxs-lookup"><span data-stu-id="94f9b-118">Calls [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) to load the cursor into memory.</span></span> <span data-ttu-id="94f9b-119">此函數會傳回資料指標的控制碼。</span><span class="sxs-lookup"><span data-stu-id="94f9b-119">This function returns a handle to the cursor.</span></span>
2.  <span data-ttu-id="94f9b-120">呼叫 [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) 並傳入資料指標控制碼。</span><span class="sxs-lookup"><span data-stu-id="94f9b-120">Calls [**SetCursor**](/windows/desktop/api/winuser/nf-winuser-setcursor) and passes in the cursor handle.</span></span>

<span data-ttu-id="94f9b-121">否則，若應用程式將 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 傳遞給 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)，則 **DefWindowProc** 函式會使用下列演算法來設定資料指標映射：</span><span class="sxs-lookup"><span data-stu-id="94f9b-121">Otherwise, if the application passes [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), the **DefWindowProc** function uses the following algorithm to set the cursor image:</span></span>

1.  <span data-ttu-id="94f9b-122">如果視窗有父代，請將 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息轉寄給父系以進行處理。</span><span class="sxs-lookup"><span data-stu-id="94f9b-122">If the window has a parent, forward the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message to the parent to handle.</span></span>
2.  <span data-ttu-id="94f9b-123">否則，如果視窗具有類別游標，請將資料指標設定為類別資料指標。</span><span class="sxs-lookup"><span data-stu-id="94f9b-123">Otherwise, if the window has a class cursor, set the cursor to the class cursor.</span></span>
3.  <span data-ttu-id="94f9b-124">如果沒有類別資料指標，請將資料指標設為箭號游標。</span><span class="sxs-lookup"><span data-stu-id="94f9b-124">If there is no class cursor, set the cursor to the arrow cursor.</span></span>

<span data-ttu-id="94f9b-125">[**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora)函數可以從資源或其中一個系統資料指標載入自訂資料指標。</span><span class="sxs-lookup"><span data-stu-id="94f9b-125">The [**LoadCursor**](/windows/desktop/api/winuser/nf-winuser-loadcursora) function can load either a custom cursor from a resource, or one of the system cursors.</span></span> <span data-ttu-id="94f9b-126">下列範例會示範如何將資料指標設定為系統手游標。</span><span class="sxs-lookup"><span data-stu-id="94f9b-126">The following example shows how to set the cursor to the system hand cursor.</span></span>


```C++
    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
```



<span data-ttu-id="94f9b-127">如果您變更游標，則在下一個滑鼠移動時，游標影像會重設，除非您攔截到 [**WM \_ SETCURSOR**](/windows/desktop/menurc/wm-setcursor) 訊息，並再次設定資料指標。</span><span class="sxs-lookup"><span data-stu-id="94f9b-127">If you change the cursor, the cursor image resets on the next mouse move, unless you intercept the [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message and set the cursor again.</span></span> <span data-ttu-id="94f9b-128">下列程式碼顯示如何處理 **WM \_ SETCURSOR**。</span><span class="sxs-lookup"><span data-stu-id="94f9b-128">The following code shows how to handle **WM\_SETCURSOR**.</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



<span data-ttu-id="94f9b-129">此程式碼會先檢查 *lParam* 的較低16位。</span><span class="sxs-lookup"><span data-stu-id="94f9b-129">This code first checks the lower 16 bits of *lParam*.</span></span> <span data-ttu-id="94f9b-130">如果 `LOWORD(lParam)` 等於 **HTCLIENT**，表示游標是在視窗的工作區上。</span><span class="sxs-lookup"><span data-stu-id="94f9b-130">If `LOWORD(lParam)` equals **HTCLIENT**, it means the cursor is over the client area of the window.</span></span> <span data-ttu-id="94f9b-131">否則，游標會在非工作區上。</span><span class="sxs-lookup"><span data-stu-id="94f9b-131">Otherwise, the cursor is over the nonclient area.</span></span> <span data-ttu-id="94f9b-132">一般而言，您應該只設定工作區的資料指標，並讓 Windows 設定非工作區的游標。</span><span class="sxs-lookup"><span data-stu-id="94f9b-132">Typically, you should only set the cursor for the client area, and let Windows set the cursor for the nonclient area.</span></span>

## <a name="next"></a><span data-ttu-id="94f9b-133">下一個</span><span class="sxs-lookup"><span data-stu-id="94f9b-133">Next</span></span>

[<span data-ttu-id="94f9b-134">使用者輸入：擴充的範例</span><span class="sxs-lookup"><span data-stu-id="94f9b-134">User Input: Extended Example</span></span>](user-input--extended-example.md)

 

 