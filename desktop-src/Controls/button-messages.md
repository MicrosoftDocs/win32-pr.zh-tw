---
title: 按鈕訊息
description: 按鈕可以將訊息傳送至其父視窗，而且父視窗可以將訊息傳送至按鈕。
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103684043"
---
# <a name="button-messages"></a><span data-ttu-id="d086c-103">按鈕訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-103">Button Messages</span></span>

<span data-ttu-id="d086c-104">按鈕可以將訊息傳送至其父視窗，而且父視窗可以將訊息傳送至按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-104">A button can send messages to its parent window, and a parent window can send messages to a button.</span></span>

<span data-ttu-id="d086c-105">本節將討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="d086c-105">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="d086c-106">傳送訊息到按鈕</span><span class="sxs-lookup"><span data-stu-id="d086c-106">Sending Messages to Buttons</span></span>](#sending-messages-to-buttons)
-   [<span data-ttu-id="d086c-107">處理按鈕的訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-107">Handling Messages from a Button</span></span>](#handling-messages-from-a-button)
-   [<span data-ttu-id="d086c-108">來自按鈕的通知訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-108">Notification Messages from Buttons</span></span>](#notification-messages-from-buttons)
-   [<span data-ttu-id="d086c-109">按鈕色彩訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-109">Button Color Messages</span></span>](#button-color-messages)
-   [<span data-ttu-id="d086c-110">按鈕預設訊息處理</span><span class="sxs-lookup"><span data-stu-id="d086c-110">Button Default Message Processing</span></span>](#button-default-message-processing)
-   [<span data-ttu-id="d086c-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d086c-111">Related topics</span></span>](#related-topics)

## <a name="sending-messages-to-buttons"></a><span data-ttu-id="d086c-112">傳送訊息到按鈕</span><span class="sxs-lookup"><span data-stu-id="d086c-112">Sending Messages to Buttons</span></span>

<span data-ttu-id="d086c-113">父視窗可以使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 函式，將訊息傳送至重迭或子視窗中的按鈕，也可以使用 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea)、 [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)、 [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)和 [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) 函數，將訊息傳送至對話方塊中的按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-113">A parent window can send messages to a button in an overlapped or child window by using the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, or it can send messages to a button in a dialog box by using the [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton), and [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) functions.</span></span>

<span data-ttu-id="d086c-114">應用程式可以使用 [**BM \_ GETCHECK**](bm-getcheck.md) 訊息來取得核取方塊或選項按鈕的核取狀態。</span><span class="sxs-lookup"><span data-stu-id="d086c-114">An application can use the [**BM\_GETCHECK**](bm-getcheck.md) message to retrieve the check state of a check box or radio button.</span></span> <span data-ttu-id="d086c-115">應用程式也可以使用 [**BM \_ >getstate**](bm-getstate.md) 訊息來取得按鈕的目前狀態， (檢查狀態、推播狀態和焦點狀態) 。</span><span class="sxs-lookup"><span data-stu-id="d086c-115">An application can also use the [**BM\_GETSTATE**](bm-getstate.md) message to retrieve the button's current states (the check state, push state, and focus state).</span></span> <span data-ttu-id="d086c-116">若要取得特定狀態的相關資訊，請在傳回的狀態值上使用位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="d086c-116">To get information about a specific state, use a bitmask on the returned state value.</span></span>

<span data-ttu-id="d086c-117">[**BM \_ SETCHECK**](bm-setcheck.md)訊息會設定核取方塊或選項按鈕的檢查狀態，而訊息則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d086c-117">The [**BM\_SETCHECK**](bm-setcheck.md) message sets the check state of a check box or radio button; the message returns zero.</span></span> <span data-ttu-id="d086c-118">[**BM \_ SETSTATE**](bm-setstate.md)訊息會設定按鈕的推送狀態; 此訊息也會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d086c-118">The [**BM\_SETSTATE**](bm-setstate.md) message sets the push state of a button; this message also returns zero.</span></span> <span data-ttu-id="d086c-119">[**BM \_ >setstyle**](bm-setstyle.md)訊息會變更按鈕的樣式。</span><span class="sxs-lookup"><span data-stu-id="d086c-119">The [**BM\_SETSTYLE**](bm-setstyle.md) message changes the style of a button.</span></span> <span data-ttu-id="d086c-120">它是專為變更類型內的按鈕樣式所設計 (例如，將核取方塊變更為自動核取方塊) 。</span><span class="sxs-lookup"><span data-stu-id="d086c-120">It is designed for changing button styles within a type (for example, changing a check box to an automatic check box).</span></span> <span data-ttu-id="d086c-121">它並非設計來變更類型 (例如，將核取方塊變更為選項按鈕) 。</span><span class="sxs-lookup"><span data-stu-id="d086c-121">It is not designed for changing between types (for example, changing a check box to a radio button).</span></span> <span data-ttu-id="d086c-122">應用程式不應該將按鈕從一種類型變更為另一種類型。</span><span class="sxs-lookup"><span data-stu-id="d086c-122">An application should not change a button from one type to another.</span></span>

<span data-ttu-id="d086c-123">[**BS \_ 點陣圖**](button-styles.md)或 [**BS \_ 圖示**](button-styles.md)樣式的按鈕會顯示點陣圖或圖示，而不是文字。</span><span class="sxs-lookup"><span data-stu-id="d086c-123">A button of the [**BS\_BITMAP**](button-styles.md) or [**BS\_ICON**](button-styles.md) style displays a bitmap or icon instead of text.</span></span> <span data-ttu-id="d086c-124">[**BM \_ SETIMAGE**](bm-setimage.md)訊息會將點陣圖或圖示的控制碼與按鈕產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d086c-124">The [**BM\_SETIMAGE**](bm-setimage.md) message associates a handle to a bitmap or icon with a button.</span></span> <span data-ttu-id="d086c-125">[**BM \_ GETIMAGE**](bm-getimage.md)訊息會抓取與按鈕相關聯之點陣圖或圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-125">The [**BM\_GETIMAGE**](bm-getimage.md) message retrieves a handle to the bitmap or icon associated with a button.</span></span>

<span data-ttu-id="d086c-126">應用程式也可以使用 [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) 訊息，在對話方塊中取出預設推播按鈕控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-126">An application can also use the [**DM\_GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) message to retrieve the identifier of the default push button control in a dialog box.</span></span> <span data-ttu-id="d086c-127">應用程式可以使用 [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) 訊息來設定對話方塊的預設推送按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-127">An application can use the [**DM\_SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) message to set the default push button for a dialog box.</span></span>

<span data-ttu-id="d086c-128">呼叫 [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) 或 [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) 函數相當於傳送 [**BM \_ SETCHECK**](bm-setcheck.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d086c-128">Calling the [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) or [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) function is equivalent to sending a [**BM\_SETCHECK**](bm-setcheck.md) message.</span></span> <span data-ttu-id="d086c-129">呼叫 [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) 函數相當於傳送 [**BM \_ GETCHECK**](bm-getcheck.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d086c-129">Calling the [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) function is equivalent to sending a [**BM\_GETCHECK**](bm-getcheck.md) message.</span></span>

## <a name="handling-messages-from-a-button"></a><span data-ttu-id="d086c-130">處理按鈕的訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-130">Handling Messages from a Button</span></span>

<span data-ttu-id="d086c-131">按鈕的通知會以 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 或 [**wm \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d086c-131">Notifications from a button are sent as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="d086c-132">您可以在每個通知的 [參考] 頁面中找到所使用訊息的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d086c-132">Information about which message is used can be found on the reference page for each notification.</span></span>

<span data-ttu-id="d086c-133">如需如何處理訊息的詳細資訊，請參閱 [控制訊息](control-messages.md)。</span><span class="sxs-lookup"><span data-stu-id="d086c-133">For more information on how to handle messages, see [Control Messages](control-messages.md).</span></span> <span data-ttu-id="d086c-134">另請參閱按鈕訊息。</span><span class="sxs-lookup"><span data-stu-id="d086c-134">See also Button Messages.</span></span>

## <a name="notification-messages-from-buttons"></a><span data-ttu-id="d086c-135">來自按鈕的通知訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-135">Notification Messages from Buttons</span></span>

<span data-ttu-id="d086c-136">當使用者按一下按鈕時，其狀態會變更，而按鈕會將通知碼（以 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的形式）傳送至其父視窗。</span><span class="sxs-lookup"><span data-stu-id="d086c-136">When the user clicks a button, its state changes, and the button sends notification codes, in the form of [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages, to its parent window.</span></span> <span data-ttu-id="d086c-137">例如，每當使用者選擇按鈕時，按鈕控制項會傳送 BN 按下的通知碼。 [ \_ ](bn-clicked.md)</span><span class="sxs-lookup"><span data-stu-id="d086c-137">For example, a push button control sends the [BN\_CLICKED](bn-clicked.md) notification code whenever the user chooses the button.</span></span> <span data-ttu-id="d086c-138">在所有情況下 (除了 [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)) 之外， *wParam* 參數的低序位字包含控制項識別碼、 *wParam* 的高序位字包含通知碼，而 *lParam* 參數則包含控制視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-138">In all cases (except for [BCN\_HOTITEMCHANGE](bcn-hotitemchange.md)), the low-order word of the *wParam* parameter contains the control identifier, the high-order word of *wParam* contains the notification code, and the *lParam* parameter contains the control window handle.</span></span>

<span data-ttu-id="d086c-139">訊息和父視窗的回應都取決於按鈕的類型、樣式和目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d086c-139">Both the message and the parent window's response depend on the type, style, and current state of the button.</span></span> <span data-ttu-id="d086c-140">以下是應用程式應該監視和處理的按鈕通知代碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-140">Following are the button notification codes an application should monitor and process.</span></span>



| <span data-ttu-id="d086c-141">通知碼</span><span class="sxs-lookup"><span data-stu-id="d086c-141">Notification code</span></span>                                                        | <span data-ttu-id="d086c-142">Description</span><span class="sxs-lookup"><span data-stu-id="d086c-142">Description</span></span>                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="d086c-143">BCN \_ HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="d086c-143">BCN\_HOTITEMCHANGE</span></span>](bcn-hotitemchange.md)                              | <span data-ttu-id="d086c-144">滑鼠已進入或離開按鈕的工作區。</span><span class="sxs-lookup"><span data-stu-id="d086c-144">The mouse entered or left the client area of a button.</span></span> |
| [<span data-ttu-id="d086c-145">BN \_ 按一下</span><span class="sxs-lookup"><span data-stu-id="d086c-145">BN\_CLICKED</span></span>](bn-clicked.md)                                            | <span data-ttu-id="d086c-146">使用者按一下按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-146">The user clicked a button.</span></span>                             |
| <span data-ttu-id="d086c-147">[BN \_DBLCLK](bn-dblclk.md) 或 [BN \_ DOUBLECLICKED](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="d086c-147">[BN\_DBLCLK](bn-dblclk.md) or [BN\_DOUBLECLICKED](bn-doubleclicked.md)</span></span> | <span data-ttu-id="d086c-148">使用者按兩下按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-148">The user double-clicked a button.</span></span>                      |
| [<span data-ttu-id="d086c-149">BN \_ DISABLE</span><span class="sxs-lookup"><span data-stu-id="d086c-149">BN\_DISABLE</span></span>](bn-disable.md)                                            | <span data-ttu-id="d086c-150">按鈕已停用。</span><span class="sxs-lookup"><span data-stu-id="d086c-150">A button is disabled.</span></span>                                  |
| <span data-ttu-id="d086c-151">[BN \_已推送](bn-pushed.md) 或 [BN \_ HILITE](bn-hilite.md)</span><span class="sxs-lookup"><span data-stu-id="d086c-151">[BN\_PUSHED](bn-pushed.md) or [BN\_HILITE](bn-hilite.md)</span></span>               | <span data-ttu-id="d086c-152">使用者按下按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-152">The user pushed a button.</span></span>                              |
| [<span data-ttu-id="d086c-153">BN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="d086c-153">BN\_KILLFOCUS</span></span>](bn-killfocus.md)                                        | <span data-ttu-id="d086c-154">按鈕失去鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="d086c-154">The button lost the keyboard focus.</span></span>                    |
| [<span data-ttu-id="d086c-155">BN \_ 油漆</span><span class="sxs-lookup"><span data-stu-id="d086c-155">BN\_PAINT</span></span>](bn-paint.md)                                                | <span data-ttu-id="d086c-156">應繪製按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-156">The button should be painted.</span></span>                          |
| [<span data-ttu-id="d086c-157">BN \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="d086c-157">BN\_SETFOCUS</span></span>](bn-setfocus.md)                                          | <span data-ttu-id="d086c-158">按鈕會取得鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="d086c-158">The button gained the keyboard focus.</span></span>                  |
| <span data-ttu-id="d086c-159">[BN \_未推送](bn-unpushed.md) 或 [BN \_ UNHILITE](bn-unhilite.md)</span><span class="sxs-lookup"><span data-stu-id="d086c-159">[BN\_UNPUSHED](bn-unpushed.md) or [BN\_UNHILITE](bn-unhilite.md)</span></span>       | <span data-ttu-id="d086c-160">此按鈕不會再推送。</span><span class="sxs-lookup"><span data-stu-id="d086c-160">The button is no longer pushed.</span></span>                        |



 

<span data-ttu-id="d086c-161">按鈕只會在具有 [**BN \_ 通知**](button-styles.md)樣式的情況下傳送 [BN \_ DISABLE](bn-disable.md)、 [BN \_ 推送](bn-pushed.md)、 [BN \_ KILLFOCUS](bn-killfocus.md)、 [BN \_ PAINT](bn-paint.md)、 [BN \_ SETFOCUS](bn-setfocus.md)和 [未推送 \_ BS](bn-unpushed.md)通知碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-161">A button sends the [BN\_DISABLE](bn-disable.md), [BN\_PUSHED](bn-pushed.md), [BN\_KILLFOCUS](bn-killfocus.md), [BN\_PAINT](bn-paint.md), [BN\_SETFOCUS](bn-setfocus.md), and [BN\_UNPUSHED](bn-unpushed.md) notification codes only if it has the [**BS\_NOTIFY**](button-styles.md) style.</span></span> <span data-ttu-id="d086c-162">[BN \_DBLCLK](bn-dblclk.md) 通知碼會自動傳送給 [**BS \_ USERBUTTON**](button-styles.md)、 [**BS \_ 單選**](button-styles.md)按鈕和 [**BS \_ OWNERDRAW**](button-styles.md) 按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-162">[BN\_DBLCLK](bn-dblclk.md) notification codes are sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="d086c-163">其他按鈕類型只有在 \_ 有 **BS \_ 通知** 樣式時，才會傳送 BN DBLCLK。</span><span class="sxs-lookup"><span data-stu-id="d086c-163">Other button types send BN\_DBLCLK only if they have the **BS\_NOTIFY** style.</span></span> <span data-ttu-id="d086c-164">無論按鈕樣式為何，所有按鈕都會傳送 BN 的已按下通知碼。 [ \_ ](bn-clicked.md)</span><span class="sxs-lookup"><span data-stu-id="d086c-164">All buttons send the [BN\_CLICKED](bn-clicked.md) notification code regardless of their button styles.</span></span>

<span data-ttu-id="d086c-165">針對 [自動] 按鈕，系統會變更推送狀態並繪製按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-165">For automatic buttons, the system changes the push state and paints the button.</span></span> <span data-ttu-id="d086c-166">在此情況下，應用程式通常只會處理按下的 [BN \_ ](bn-clicked.md) ，並 [BN \_ DBLCLK](bn-dblclk.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-166">In this case, the application typically processes only the [BN\_CLICKED](bn-clicked.md) and [BN\_DBLCLK](bn-dblclk.md) notification codes.</span></span> <span data-ttu-id="d086c-167">對於非自動的按鈕，應用程式通常會傳送訊息來變更按鈕的狀態，以回應通知碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-167">For buttons that are not automatic, the application typically responds to the notification code by sending a message to change the state of the button.</span></span> <span data-ttu-id="d086c-168">如需將訊息傳送至按鈕的相關資訊，請參閱 [將訊息傳送至按鈕](#sending-messages-to-buttons)。</span><span class="sxs-lookup"><span data-stu-id="d086c-168">For information about sending messages to buttons, see [Sending Messages to Buttons](#sending-messages-to-buttons).</span></span>

<span data-ttu-id="d086c-169">當使用者選取主控描繪按鈕時，按鈕會傳送包含要繪製之控制項識別碼的 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息，以及其維度和狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d086c-169">When the user selects an owner-drawn button, the button sends its parent window a [**WM\_DRAWITEM**](wm-drawitem.md) message containing the identifier of the control to be drawn and information about its dimensions and state.</span></span>

## <a name="button-color-messages"></a><span data-ttu-id="d086c-170">按鈕色彩訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-170">Button Color Messages</span></span>

<span data-ttu-id="d086c-171">系統會為按鈕提供預設的色彩值。</span><span class="sxs-lookup"><span data-stu-id="d086c-171">The system provides default color values for buttons.</span></span> <span data-ttu-id="d086c-172">應用程式可以藉由呼叫 [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) 函式來取得這些色彩的預設值，或藉由呼叫 [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) 函數來設定值。</span><span class="sxs-lookup"><span data-stu-id="d086c-172">An application can retrieve the default values for these colors by calling the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) function, or set the values by calling the [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) function.</span></span> <span data-ttu-id="d086c-173">下表顯示預設的按鈕色彩值。</span><span class="sxs-lookup"><span data-stu-id="d086c-173">The following table shows the default button-color values.</span></span>



| <span data-ttu-id="d086c-174">值</span><span class="sxs-lookup"><span data-stu-id="d086c-174">Value</span></span>               | <span data-ttu-id="d086c-175">元素著色</span><span class="sxs-lookup"><span data-stu-id="d086c-175">Element colored</span></span>                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d086c-176">色彩 \_ BTNFACE</span><span class="sxs-lookup"><span data-stu-id="d086c-176">COLOR\_BTNFACE</span></span>      | <span data-ttu-id="d086c-177">按鈕臉部。</span><span class="sxs-lookup"><span data-stu-id="d086c-177">Button faces.</span></span>                                                                                                              |
| <span data-ttu-id="d086c-178">色彩 \_ BTNHIGHLIGHT</span><span class="sxs-lookup"><span data-stu-id="d086c-178">COLOR\_BTNHIGHLIGHT</span></span> | <span data-ttu-id="d086c-179">醒目提示區域 (按鈕的上方和左邊緣) 。</span><span class="sxs-lookup"><span data-stu-id="d086c-179">Highlight area (the top and left edges) of a button.</span></span>                                                                       |
| <span data-ttu-id="d086c-180">色彩 \_ BTNSHADOW</span><span class="sxs-lookup"><span data-stu-id="d086c-180">COLOR\_BTNSHADOW</span></span>    | <span data-ttu-id="d086c-181">陰影區域 (按鈕的下邊緣和右邊緣) 。</span><span class="sxs-lookup"><span data-stu-id="d086c-181">Shadow area (the bottom and right edges) of a button.</span></span>                                                                      |
| <span data-ttu-id="d086c-182">色彩 \_ BTNTEXT</span><span class="sxs-lookup"><span data-stu-id="d086c-182">COLOR\_BTNTEXT</span></span>      | <span data-ttu-id="d086c-183">一般 (nongrayed 按鈕中) 文字。</span><span class="sxs-lookup"><span data-stu-id="d086c-183">Regular (nongrayed) text in buttons.</span></span>                                                                                       |
| <span data-ttu-id="d086c-184">色彩 \_ GRAYTEXT</span><span class="sxs-lookup"><span data-stu-id="d086c-184">COLOR\_GRAYTEXT</span></span>     | <span data-ttu-id="d086c-185">停用 (灰色) 按鈕中的文字。</span><span class="sxs-lookup"><span data-stu-id="d086c-185">Disabled (gray) text in buttons.</span></span> <span data-ttu-id="d086c-186">如果目前的顯示驅動程式不支援純灰色色彩，此色彩會設為0。</span><span class="sxs-lookup"><span data-stu-id="d086c-186">This color is set to 0 if the current display driver does not support a solid gray color.</span></span> |
| <span data-ttu-id="d086c-187">色彩 \_ 視窗</span><span class="sxs-lookup"><span data-stu-id="d086c-187">COLOR\_WINDOW</span></span>       | <span data-ttu-id="d086c-188">視窗背景。</span><span class="sxs-lookup"><span data-stu-id="d086c-188">Window backgrounds.</span></span>                                                                                                        |
| <span data-ttu-id="d086c-189">色彩 \_ WINDOWFRAME</span><span class="sxs-lookup"><span data-stu-id="d086c-189">COLOR\_WINDOWFRAME</span></span>  | <span data-ttu-id="d086c-190">窗框。</span><span class="sxs-lookup"><span data-stu-id="d086c-190">Window frames.</span></span>                                                                                                             |
| <span data-ttu-id="d086c-191">色彩 \_ WINDOWTEXT</span><span class="sxs-lookup"><span data-stu-id="d086c-191">COLOR\_WINDOWTEXT</span></span>   | <span data-ttu-id="d086c-192">Windows 中的文字。</span><span class="sxs-lookup"><span data-stu-id="d086c-192">Text in windows.</span></span>                                                                                                           |



 

<span data-ttu-id="d086c-193">不過，呼叫 [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) 會影響所有的應用程式，因此您不應該呼叫此函式來自訂應用程式的按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-193">However, calling [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affects all applications, so you should not call this function to customize buttons for your application.</span></span>

<span data-ttu-id="d086c-194">系統會在繪製按鈕之前，將 [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) 訊息傳送至按鈕的父視窗。</span><span class="sxs-lookup"><span data-stu-id="d086c-194">The system sends a [**WM\_CTLCOLORBTN**](wm-ctlcolorbtn.md) message to a button's parent window before drawing a button.</span></span> <span data-ttu-id="d086c-195">此訊息包含按鈕之裝置內容的控制碼，以及子視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-195">This message contains a handle to the button's device context and a handle to the child window.</span></span> <span data-ttu-id="d086c-196">父視窗可以使用這些控點來變更按鈕的文字和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="d086c-196">The parent window can use these handles to change the button's text and background colors.</span></span> <span data-ttu-id="d086c-197">不過，只有主控描繪的按鈕會回應處理訊息的父視窗。</span><span class="sxs-lookup"><span data-stu-id="d086c-197">However, only owner-drawn buttons respond to the parent window processing the message.</span></span>

## <a name="button-default-message-processing"></a><span data-ttu-id="d086c-198">按鈕預設訊息處理</span><span class="sxs-lookup"><span data-stu-id="d086c-198">Button Default Message Processing</span></span>

<span data-ttu-id="d086c-199">預先定義之按鈕控制項視窗類別的視窗程式，會針對按鈕控制項程式未處理的所有訊息執行預設處理。</span><span class="sxs-lookup"><span data-stu-id="d086c-199">The window procedure for the predefined button control window class carries out default processing for all messages that the button control procedure does not process.</span></span> <span data-ttu-id="d086c-200">當 button control 程式針對任何訊息傳回 **FALSE** 時，預先定義的視窗程式會檢查訊息，並執行下表所列的預設動作。</span><span class="sxs-lookup"><span data-stu-id="d086c-200">When the button control procedure returns **FALSE** for any message, the predefined window procedure checks the messages and performs the default actions listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d086c-201">訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-201">Message</span></span></th>
<th><span data-ttu-id="d086c-202">預設動作</span><span class="sxs-lookup"><span data-stu-id="d086c-202">Default action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d086c-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span></span></td>
<td><span data-ttu-id="d086c-204">將 <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> 和 <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> 訊息傳送給按鈕，並將父視窗傳送 <a href="bn-clicked.md">BN_CLICKED</a> 的通知碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-204">Sends the button a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> and a <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> message, and sends the parent window a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="d086c-206">傳回按鈕的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="d086c-206">Returns the check state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-208">傳回與按鈕相關聯之點陣圖或圖示的控制碼，如果按鈕沒有點陣圖或圖示，則為 <strong>Null</strong> 。</span><span class="sxs-lookup"><span data-stu-id="d086c-208">Returns a handle to the bitmap or icon associated with the button or <strong>NULL</strong> if the button has no bitmap or icon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-210">傳回按鈕的目前檢查狀態、推播狀態和焦點狀態。</span><span class="sxs-lookup"><span data-stu-id="d086c-210">Returns the current check state, push state, and focus state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="d086c-212">設定選項按鈕和核取方塊樣式的檢查狀態。</span><span class="sxs-lookup"><span data-stu-id="d086c-212">Sets the check state for all styles of radio buttons and check boxes.</span></span> <span data-ttu-id="d086c-213">如果選項按鈕的 <em>wParam</em> 參數大於零，則按鈕會獲得 <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> 的樣式。</span><span class="sxs-lookup"><span data-stu-id="d086c-213">If the <em>wParam</em> parameter is greater than zero for radio buttons, the button is given the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> style.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-215">將指定的點陣圖或圖示控制碼與按鈕建立關聯，並將控制碼傳回至上一個點陣圖或圖示。</span><span class="sxs-lookup"><span data-stu-id="d086c-215">Associates the specified bitmap or icon handle with the button and returns a handle to the previous bitmap or icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-217">設定按鈕的推送狀態。</span><span class="sxs-lookup"><span data-stu-id="d086c-217">Sets the push state of the button.</span></span> <span data-ttu-id="d086c-218">針對主控描繪按鈕，如果按鈕的狀態已變更，則會將 <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> 訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="d086c-218">For owner-drawn buttons, a <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message is sent to the parent window if the state of the button has changed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-220">設定按鈕樣式。</span><span class="sxs-lookup"><span data-stu-id="d086c-220">Sets the button style.</span></span> <span data-ttu-id="d086c-221">如果 <em>lParam</em> 參數的低序位字是 <strong>TRUE</strong>，則會重新繪製按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-221">If the low-order word of the <em>lParam</em> parameter is <strong>TRUE</strong>, the button is redrawn.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span></span></td>
<td><span data-ttu-id="d086c-223">當使用者按下加號 (+) 或等於 (=) 索引鍵時，檢查核取方塊或 [自動] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="d086c-223">Checks a check box or automatic check box when the user presses the plus (+) or equal (=) keys.</span></span> <span data-ttu-id="d086c-224">當使用者按下減號 (-) 鍵時，清除核取方塊或 [自動] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="d086c-224">Clears a check box or automatic check box when the user presses the minus (–) key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-226">繪製按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-226">Paints the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span></span></td>
<td><span data-ttu-id="d086c-228">清除擁有者繪製按鈕的背景。</span><span class="sxs-lookup"><span data-stu-id="d086c-228">Erases the background for owner-drawn buttons.</span></span> <span data-ttu-id="d086c-229">其他按鈕的背景會在 <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> 中清除，並 <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> 處理。</span><span class="sxs-lookup"><span data-stu-id="d086c-229">The backgrounds of other buttons are erased as part of the <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> and <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-231">傳回值，這個值表示預設按鈕程式所處理的輸入類型，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="d086c-231">Returns values that indicate the type of input processed by the default button procedure, as shown in the following table.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d086c-232">按鈕樣式</span><span class="sxs-lookup"><span data-stu-id="d086c-232">Button style</span></span></th>
<th><span data-ttu-id="d086c-233">傳回</span><span class="sxs-lookup"><span data-stu-id="d086c-233">Returns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d086c-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="d086c-235">DLGC_WANTCHARS |DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d086c-235">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d086c-237">DLGC_RADIOBUTTON |DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d086c-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="d086c-239">DLGC_WANTCHARS |DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d086c-239">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d086c-241">DLGC_DEFPUSHBUTTON |DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d086c-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span></span></td>
<td><span data-ttu-id="d086c-243">DLGC_STATIC</span><span class="sxs-lookup"><span data-stu-id="d086c-243">DLGC_STATIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d086c-245">DLGC_UNDEFPUSHBUTTON |DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d086c-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="d086c-247">DLGC_RADIOBUTTON |DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d086c-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span></span></td>
<td><span data-ttu-id="d086c-249">傳回目前字型的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-249">Returns a handle to the current font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span></span></td>
<td><span data-ttu-id="d086c-251">如果使用者按下空格鍵，則推送按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-251">Pushes the button if the user presses the SPACEBAR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span></span></td>
<td><span data-ttu-id="d086c-253">除了 TAB 鍵之外，也會釋放所有案例的滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="d086c-253">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="d086c-255">從按鈕中移除焦點矩形。</span><span class="sxs-lookup"><span data-stu-id="d086c-255">Removes the focus rectangle from a button.</span></span> <span data-ttu-id="d086c-256">針對推播按鈕和預設的推播按鈕，焦點矩形會失效。</span><span class="sxs-lookup"><span data-stu-id="d086c-256">For push buttons and default push buttons, the focus rectangle is invalidated.</span></span> <span data-ttu-id="d086c-257">如果按鈕具有滑鼠捕捉，則會釋出抓取，並不會按一下按鈕，而且會移除任何推送狀態。</span><span class="sxs-lookup"><span data-stu-id="d086c-257">If the button has the mouse capture, the capture is released, the button is not clicked, and any push state is removed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span></span></td>
<td><span data-ttu-id="d086c-259">將 <a href="bn-dblclk.md">BN_DBLCLK</a> 通知程式碼傳送至選項按鈕和主控描繪按鈕的父視窗。</span><span class="sxs-lookup"><span data-stu-id="d086c-259">Sends a <a href="bn-dblclk.md">BN_DBLCLK</a> notification code to the parent window for radio buttons and owner-drawn buttons.</span></span> <span data-ttu-id="d086c-260">針對其他按鈕，按兩下會被視為 <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> 的訊息來處理。</span><span class="sxs-lookup"><span data-stu-id="d086c-260">For other buttons, a double-click is processed as a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span></span></td>
<td><span data-ttu-id="d086c-262">如果滑鼠游標的位置在按鈕的用戶端矩形內，則會反白顯示按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-262">Highlights the button if the position of the mouse cursor is within the button's client rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span></span></td>
<td><span data-ttu-id="d086c-264">如果按鈕具有滑鼠捕捉，則放開滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="d086c-264">Releases the mouse capture if the button had the mouse capture.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-266">如果按鈕具有滑鼠捕捉，則執行與 <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>相同的動作。</span><span class="sxs-lookup"><span data-stu-id="d086c-266">Performs the same action as <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, if the button has the mouse capture.</span></span> <span data-ttu-id="d086c-267">否則，就不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="d086c-267">Otherwise, no action is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span></span></td>
<td><span data-ttu-id="d086c-269">將任何 <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> 按鈕變成 <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> 按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-269">Turns any <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> button into a <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> button.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span></span></td>
<td><span data-ttu-id="d086c-271">如果按鈕控制項是群組方塊，則會傳回 HTTRANSPARENT。</span><span class="sxs-lookup"><span data-stu-id="d086c-271">Returns HTTRANSPARENT, if the button control is a group box.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span></span></td>
<td><span data-ttu-id="d086c-273">根據按鈕的樣式和目前狀態繪製按鈕。</span><span class="sxs-lookup"><span data-stu-id="d086c-273">Draws the button according to its style and current state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="d086c-275">在按鈕上繪製焦點矩形以取得焦點。</span><span class="sxs-lookup"><span data-stu-id="d086c-275">Draws a focus rectangle on the button getting the focus.</span></span> <span data-ttu-id="d086c-276">針對選項按鈕和自動選項按鈕，父視窗會傳送 <a href="bn-clicked.md">BN_CLICKED</a> 通知碼。</span><span class="sxs-lookup"><span data-stu-id="d086c-276">For radio buttons and automatic radio buttons, the parent window is sent a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span></span></td>
<td><span data-ttu-id="d086c-278">設定新的字型，並選擇性地更新視窗。</span><span class="sxs-lookup"><span data-stu-id="d086c-278">Sets a new font and optionally updates the window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d086c-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span></span></td>
<td><span data-ttu-id="d086c-280">設定按鈕的文字。</span><span class="sxs-lookup"><span data-stu-id="d086c-280">Sets the text of the button.</span></span> <span data-ttu-id="d086c-281">在群組方塊的案例中，訊息會繪製預先存在的文字，然後再以新的文字重新繪製群組方塊。</span><span class="sxs-lookup"><span data-stu-id="d086c-281">In the case of a group box, the message paints over the preexisting text before repainting the group box with the new text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d086c-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="d086c-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span></span></td>
<td><span data-ttu-id="d086c-283">除了 TAB 鍵之外，也會釋放所有案例的滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="d086c-283">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d086c-284">預先定義的視窗程式會將所有其他訊息傳遞至 [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) 函式，以進行預設處理。</span><span class="sxs-lookup"><span data-stu-id="d086c-284">The predefined window procedure passes all other messages to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function for default processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d086c-285">相關主題</span><span class="sxs-lookup"><span data-stu-id="d086c-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d086c-286">控制訊息</span><span class="sxs-lookup"><span data-stu-id="d086c-286">Control Messages</span></span>](control-messages.md)
</dt> </dl>

 

 