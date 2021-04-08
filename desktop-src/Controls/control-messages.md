---
title: 控制訊息
description: 本章節包含如何使用 Windows 訊息與控制項通訊的相關資訊。
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103842944"
---
# <a name="control-messages"></a><span data-ttu-id="8a93c-103">控制訊息</span><span class="sxs-lookup"><span data-stu-id="8a93c-103">Control Messages</span></span>

<span data-ttu-id="8a93c-104">本章節包含如何使用 Windows 訊息與控制項通訊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8a93c-104">This section contains information about how Windows messages are used to communicate with controls.</span></span>

<span data-ttu-id="8a93c-105">討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="8a93c-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="8a93c-106">傳送至通用控制項的訊息</span><span class="sxs-lookup"><span data-stu-id="8a93c-106">Messages to Common Controls</span></span>](#messages-to-common-controls)
-   [<span data-ttu-id="8a93c-107">來自控制項的通知</span><span class="sxs-lookup"><span data-stu-id="8a93c-107">Notifications from Controls</span></span>](#notifications-from-controls)
-   [<span data-ttu-id="8a93c-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a93c-108">Related topics</span></span>](#related-topics)

## <a name="messages-to-common-controls"></a><span data-ttu-id="8a93c-109">傳送至通用控制項的訊息</span><span class="sxs-lookup"><span data-stu-id="8a93c-109">Messages to Common Controls</span></span>

<span data-ttu-id="8a93c-110">由於通用控制項是 windows，因此應用程式可以使用常見的 Microsoft Win32 訊息（例如 [**wm \_ GETFONT**](/windows/desktop/winmsg/wm-getfont) 或 [**wm \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)）來與其通訊。</span><span class="sxs-lookup"><span data-stu-id="8a93c-110">Because common controls are windows, an application can communicate with them by using common Microsoft Win32 messages such as [**WM\_GETFONT**](/windows/desktop/winmsg/wm-getfont) or [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span> <span data-ttu-id="8a93c-111">此外，每個通用控制項的視窗類別都支援一組控制項特定的訊息。</span><span class="sxs-lookup"><span data-stu-id="8a93c-111">In addition, the window class of each common control supports a set of control-specific messages.</span></span> <span data-ttu-id="8a93c-112">一般而言，應用程式會使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 或 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) 將訊息傳遞至控制項， (通常會在傳回值) 中接收資訊。</span><span class="sxs-lookup"><span data-stu-id="8a93c-112">Typically, an application uses [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) to pass messages to the control (often receiving information in the return value).</span></span>

<span data-ttu-id="8a93c-113">某些常見的控制項也有一組可供應用程式使用的宏，而不是 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)。</span><span class="sxs-lookup"><span data-stu-id="8a93c-113">Some common controls also have a set of macros that an application can use instead of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="8a93c-114">這些宏通常比函數更容易使用。</span><span class="sxs-lookup"><span data-stu-id="8a93c-114">The macros are typically easier to use than the functions.</span></span> <span data-ttu-id="8a93c-115">下列範例程式碼會先使用原始訊息來抓取所選樹狀檢視專案的文字，第二個則是使用對等宏。</span><span class="sxs-lookup"><span data-stu-id="8a93c-115">The following example code retrieves the text of the selected tree-view item, first by using the raw messages, and second by using the equivalent macros.</span></span> <span data-ttu-id="8a93c-116">假設 *hwnd* 是控制項視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8a93c-116">Assume that *hwnd* is the handle of the control window.</span></span>


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



<span data-ttu-id="8a93c-117">當系統色彩設定進行變更時，Windows 會將 [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) 訊息傳送至所有最上層視窗。</span><span class="sxs-lookup"><span data-stu-id="8a93c-117">When a change is made to the system color settings, Windows sends a [**WM\_SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) message to all top-level windows.</span></span> <span data-ttu-id="8a93c-118">您的最上層視窗必須將 **WM \_ SYSCOLORCHANGE** 訊息轉寄到其通用控制項; 否則，將不會通知控制項色彩變更。</span><span class="sxs-lookup"><span data-stu-id="8a93c-118">Your top-level window must forward the **WM\_SYSCOLORCHANGE** message to its common controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="8a93c-119">轉送訊息可確保通用控制項使用的色彩與其他使用者介面物件所使用的色彩一致。</span><span class="sxs-lookup"><span data-stu-id="8a93c-119">Forwarding the message ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="8a93c-120">例如，工具列控制項會使用「立體物件」色彩來繪製其按鈕。</span><span class="sxs-lookup"><span data-stu-id="8a93c-120">For example, a toolbar control uses the "3-D Objects" color to draw its buttons.</span></span> <span data-ttu-id="8a93c-121">如果使用者變更立體物件的色彩，但卻未將 **WM \_ SYSCOLORCHANGE** 訊息轉寄至工具列，工具列按鈕將會維持原來的色彩 (甚至會變更為舊色彩和新色彩的組合) 而系統中其他按鈕的色彩也會變更。</span><span class="sxs-lookup"><span data-stu-id="8a93c-121">If the user changes the 3-D Object's color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color (or even change to a combination of old and new colors) while the color of other buttons in the system changes.</span></span>

## <a name="notifications-from-controls"></a><span data-ttu-id="8a93c-122">來自控制項的通知</span><span class="sxs-lookup"><span data-stu-id="8a93c-122">Notifications from Controls</span></span>

<span data-ttu-id="8a93c-123">控制項是子視窗，會在控制項中發生事件（通常是由使用者輸入觸發）時，將通知訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="8a93c-123">Controls are child windows that send notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="8a93c-124">應用程式仰賴這些通知訊息來判斷使用者要其採取的動作。</span><span class="sxs-lookup"><span data-stu-id="8a93c-124">The application relies on these notification messages to determine what action the user wants it to take.</span></span> <span data-ttu-id="8a93c-125">除了 trackbars，它會使用 [**wm \_ HSCROLL**](wm-hscroll.md) 和 [**wm \_ VSCROLL**](wm-vscroll.md) 訊息來通知其父系的變更，通用控制項會以 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 或 [**wm \_ 通知**](wm-notify.md) 訊息的形式傳送通知，如通知的參考主題中所指定。</span><span class="sxs-lookup"><span data-stu-id="8a93c-125">Except for trackbars, which use the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to notify their parent of changes, common controls send notifications as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages, as specified in the reference topic for the notification.</span></span> <span data-ttu-id="8a93c-126">一般情況下，較舊的通知 (已在 API 中的較長時間) 使用 **WM \_ 命令**。</span><span class="sxs-lookup"><span data-stu-id="8a93c-126">Typically, older notifications (those that have been in the API for a long time) use **WM\_COMMAND**.</span></span>

<span data-ttu-id="8a93c-127">[**WM \_ 通知**](wm-notify.md)的 *lParam* 參數是 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的位址，或是包含 **NMHDR** 作為其第一個成員的較大結構位址。</span><span class="sxs-lookup"><span data-stu-id="8a93c-127">The *lParam* parameter of [**WM\_NOTIFY**](wm-notify.md) is either the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure or the address of a larger structure that includes **NMHDR** as its first member.</span></span> <span data-ttu-id="8a93c-128">結構包含通知碼，並識別傳送通知訊息的通用控制項。</span><span class="sxs-lookup"><span data-stu-id="8a93c-128">The structure contains the notification code and identifies the common control that sent the notification message.</span></span> <span data-ttu-id="8a93c-129">其餘結構成員（如果有的話）的意義會根據通知碼而有所不同。</span><span class="sxs-lookup"><span data-stu-id="8a93c-129">The meaning of the remaining structure members, if any, varies depending on the notification code.</span></span>

<span data-ttu-id="8a93c-130">每種類型的通用控制項都有一組對應的通知碼。</span><span class="sxs-lookup"><span data-stu-id="8a93c-130">Each type of common control has a corresponding set of notification codes.</span></span> <span data-ttu-id="8a93c-131">通用控制項程式庫也提供可由一個以上的通用控制項類型傳送的通知碼。</span><span class="sxs-lookup"><span data-stu-id="8a93c-131">The common control library also provides notification codes that can be sent by more than one type of common control.</span></span> <span data-ttu-id="8a93c-132">請參閱相關控制項的檔，以判斷要傳送的通知碼，以及他們所採用的格式。</span><span class="sxs-lookup"><span data-stu-id="8a93c-132">See the documentation for the control of interest to determine which notification codes it will send and what format they take.</span></span>

<span data-ttu-id="8a93c-133">如需顯示如何處理 [**WM \_ 通知**](wm-notify.md) 訊息的程式碼範例，請參閱該訊息的參考主題。</span><span class="sxs-lookup"><span data-stu-id="8a93c-133">For example code showing how to handle [**WM\_NOTIFY**](wm-notify.md) messages, see the reference topic for that message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a93c-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="8a93c-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a93c-135">一般控制項參考</span><span class="sxs-lookup"><span data-stu-id="8a93c-135">General Control Reference</span></span>](common-control-reference.md)
</dt> </dl>

 

 
