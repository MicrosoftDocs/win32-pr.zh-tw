---
title: 自訂控制項
description: 本節包含應用程式定義或自訂控制項的相關資訊。
ms.assetid: 220f7058-db04-46d0-acee-ed5e676790b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e82ed9394ec06257e524153b86ef487f4507f35b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093332"
---
# <a name="custom-controls"></a><span data-ttu-id="d69ed-103">自訂控制項</span><span class="sxs-lookup"><span data-stu-id="d69ed-103">Custom Controls</span></span>

<span data-ttu-id="d69ed-104">本節包含應用程式定義或自訂控制項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d69ed-104">This section contains information about application-defined or custom controls.</span></span>

<span data-ttu-id="d69ed-105">討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="d69ed-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="d69ed-106">建立 Owner-Drawn 控制項</span><span class="sxs-lookup"><span data-stu-id="d69ed-106">Creating Owner-Drawn Controls</span></span>](#creating-owner-drawn-controls)
-   [<span data-ttu-id="d69ed-107">子類別化現有控制項的視窗類別</span><span class="sxs-lookup"><span data-stu-id="d69ed-107">Subclassing the Window Class of an Existing Control</span></span>](#subclassing-the-window-class-of-an-existing-control)
-   [<span data-ttu-id="d69ed-108">執行 Application-Defined 視窗類別</span><span class="sxs-lookup"><span data-stu-id="d69ed-108">Implementing an Application-Defined Window Class</span></span>](#implementing-an-application-defined-window-class)
-   [<span data-ttu-id="d69ed-109">從控制項傳送通知</span><span class="sxs-lookup"><span data-stu-id="d69ed-109">Sending Notifications from a Control</span></span>](#sending-notifications-from-a-control)
-   [<span data-ttu-id="d69ed-110">協助工具</span><span class="sxs-lookup"><span data-stu-id="d69ed-110">Accessibility</span></span>](#accessibility)
-   [<span data-ttu-id="d69ed-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d69ed-111">Related topics</span></span>](#related-topics)

## <a name="creating-owner-drawn-controls"></a><span data-ttu-id="d69ed-112">建立 Owner-Drawn 控制項</span><span class="sxs-lookup"><span data-stu-id="d69ed-112">Creating Owner-Drawn Controls</span></span>

<span data-ttu-id="d69ed-113">您可以使用主控描繪樣式旗標來建立按鈕、功能表、靜態文字控制項、清單方塊和下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="d69ed-113">Buttons, menus, static text controls, list boxes, and combo boxes can be created with an owner-drawn style flag.</span></span> <span data-ttu-id="d69ed-114">當控制項具有主控描繪的樣式時，系統會像往常一樣處理使用者與控制項的互動，執行這類工作，像是在使用者選擇按鈕和通知按鈕的事件擁有者時偵測。</span><span class="sxs-lookup"><span data-stu-id="d69ed-114">When a control has the owner-drawn style, the system handles the user's interaction with the control as usual, performing such tasks as detecting when a user has chosen a button and notifying the button's owner of the event.</span></span> <span data-ttu-id="d69ed-115">不過，因為控制項是主控描繪的，所以控制項的父視窗會負責控制項的視覺外觀。</span><span class="sxs-lookup"><span data-stu-id="d69ed-115">However, because the control is owner-drawn, the parent window of the control is responsible for the visual appearance of the control.</span></span> <span data-ttu-id="d69ed-116">每次必須繪製控制項時，父視窗就會收到訊息。</span><span class="sxs-lookup"><span data-stu-id="d69ed-116">The parent window receives a message whenever the control must be drawn.</span></span>

<span data-ttu-id="d69ed-117">若為按鈕和靜態文字控制項，擁有者繪製的樣式會影響系統繪製整個控制項的方式。</span><span class="sxs-lookup"><span data-stu-id="d69ed-117">For buttons and static text controls, the owner-drawn style affects how the system draws the entire control.</span></span> <span data-ttu-id="d69ed-118">針對清單方塊和下拉式方塊，父視窗會繪製控制項內的專案，而控制項則會繪製自己的外框。</span><span class="sxs-lookup"><span data-stu-id="d69ed-118">For list boxes and combo boxes, the parent window draws the items within the control, and the control draws its own outline.</span></span> <span data-ttu-id="d69ed-119">例如，應用程式可以自訂清單方塊，使其在清單中的每個專案旁顯示一個小點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d69ed-119">For example, an application can customize a list box so that it displays a small bitmap next to each item in the list.</span></span>

<span data-ttu-id="d69ed-120">下列範例程式碼顯示如何建立主控描繪的靜態文字控制項。</span><span class="sxs-lookup"><span data-stu-id="d69ed-120">The following example code shows how to create an owner-drawn static text control.</span></span> <span data-ttu-id="d69ed-121">假設已定義 Unicode。</span><span class="sxs-lookup"><span data-stu-id="d69ed-121">Assume that Unicode is defined.</span></span>


```
// g_myStatic is a global HWND variable.
g_myStatic = CreateWindowEx(0, L"STATIC", L"Some static text", 
            WS_CHILD | WS_VISIBLE | SS_OWNERDRAW, 
            25, 125, 150, 20, hDlg, 0, 0, 0);
```



<span data-ttu-id="d69ed-122">在下列範例中，從包含在上一個範例中所建立之控制項之對話方塊的視窗程式中，會使用預設字型以自訂色彩顯示文字來處理 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="d69ed-122">In the following example, from the window procedure for the dialog box that contains the control created in the previous example, the [**WM\_DRAWITEM**](wm-drawitem.md) message is handled by displaying the text in a custom color, using the default font.</span></span> <span data-ttu-id="d69ed-123">請注意，您不需要在處理 **WM \_ DRAWITEM** 時呼叫 [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint)和 [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) 。</span><span class="sxs-lookup"><span data-stu-id="d69ed-123">Note that you do not need to call [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/winuser/nf-winuser-endpaint) when handling **WM\_DRAWITEM**.</span></span>


```
case WM_DRAWITEM:
{
    LPDRAWITEMSTRUCT pDIS = (LPDRAWITEMSTRUCT)lParam;
    if (pDIS->hwndItem == g_myStatic)
    {
        SetTextColor(pDIS->hDC, RGB(100, 0, 100));
        WCHAR staticText[99];
        int len = SendMessage(myStatic, WM_GETTEXT, 
            ARRAYSIZE(staticText), (LPARAM)staticText);
        TextOut(pDIS->hDC, pDIS->rcItem.left, pDIS->rcItem.top, staticText, len);
    }
    return TRUE;
}
```



<span data-ttu-id="d69ed-124">如需主控描繪控制項的詳細資訊，請參閱建立主控描繪 [清單方塊](using-list-boxes.md) 和 [擁有者繪製](about-combo-boxes.md)的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="d69ed-124">For more information about owner-drawn controls, see [Creating an Owner-drawn List Box](using-list-boxes.md) and [Owner Drawn Combo Boxes](about-combo-boxes.md).</span></span>

## <a name="subclassing-the-window-class-of-an-existing-control"></a><span data-ttu-id="d69ed-125">子類別化現有控制項的視窗類別</span><span class="sxs-lookup"><span data-stu-id="d69ed-125">Subclassing the Window Class of an Existing Control</span></span>

<span data-ttu-id="d69ed-126">將現有控制項子類別化是另一種建立自訂控制項的方式。</span><span class="sxs-lookup"><span data-stu-id="d69ed-126">Subclassing an existing control is another way to create a custom control.</span></span> <span data-ttu-id="d69ed-127">子類別程式可以藉由處理影響所選行為的訊息，來改變控制項的選取行為。</span><span class="sxs-lookup"><span data-stu-id="d69ed-127">The subclass procedure can alter selected behaviors of the control by processing those messages that affect the selected behaviors.</span></span> <span data-ttu-id="d69ed-128">所有其他訊息都會傳遞至控制項的原始視窗程式。</span><span class="sxs-lookup"><span data-stu-id="d69ed-128">All other messages pass to the original window procedure for the control.</span></span> <span data-ttu-id="d69ed-129">例如，應用程式可以將控制項子類別化並處理 [**WM \_ 油漆**](/windows/desktop/gdi/wm-paint) 訊息，以在唯讀、單行編輯控制項中的文字旁邊顯示小型點陣圖。</span><span class="sxs-lookup"><span data-stu-id="d69ed-129">For example, an application can display a small bitmap next to the text in a read-only, single-line edit control by subclassing the control and processing the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="d69ed-130">如需詳細資訊，請參閱 [關於視窗程式](/windows/desktop/winmsg/about-window-procedures) 和子類別化 [控制項](subclassing-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="d69ed-130">For more information, see [About Window Procedures](/windows/desktop/winmsg/about-window-procedures) and [Subclassing Controls](subclassing-overview.md).</span></span>

## <a name="implementing-an-application-defined-window-class"></a><span data-ttu-id="d69ed-131">執行 Application-Defined 視窗類別</span><span class="sxs-lookup"><span data-stu-id="d69ed-131">Implementing an Application-Defined Window Class</span></span>

<span data-ttu-id="d69ed-132">若要建立未根據現有控制項明確地建立的控制項，應用程式必須建立並註冊視窗類別。</span><span class="sxs-lookup"><span data-stu-id="d69ed-132">To create a control that is not explicitly based on an existing control, the application must create and register a window class.</span></span> <span data-ttu-id="d69ed-133">註冊自訂控制項之應用程式定義視窗類別的程式，與註冊一般視窗的類別相同。</span><span class="sxs-lookup"><span data-stu-id="d69ed-133">The process for registering an application-defined window class for a custom control is the same as registering a class for an ordinary window.</span></span> <span data-ttu-id="d69ed-134">若要建立自訂控制項，請在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數或對話方塊範本中指定視窗類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="d69ed-134">To create a custom control, specify the name of the window class in the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or in a dialog box template.</span></span> <span data-ttu-id="d69ed-135">每個類別都必須有唯一的名稱、對應的視窗程式和其他資訊。</span><span class="sxs-lookup"><span data-stu-id="d69ed-135">Each class must have a unique name, a corresponding window procedure, and other information.</span></span>

<span data-ttu-id="d69ed-136">視窗程式至少會繪製控制項。</span><span class="sxs-lookup"><span data-stu-id="d69ed-136">At a minimum, the window procedure draws the control.</span></span> <span data-ttu-id="d69ed-137">如果應用程式使用控制項來讓使用者輸入資訊，則視窗程式也會處理鍵盤和滑鼠的輸入訊息，並將通知訊息傳送至父視窗。</span><span class="sxs-lookup"><span data-stu-id="d69ed-137">If an application uses the control to let the user type information, the window procedure also processes input messages from the keyboard and mouse and sends notification messages to the parent window.</span></span> <span data-ttu-id="d69ed-138">此外，如果控制項支援控制訊息，則視窗程式會處理由父視窗或其他視窗傳送給它的訊息。</span><span class="sxs-lookup"><span data-stu-id="d69ed-138">In addition, if the control supports control messages, the window procedure processes messages sent to it by the parent window or other windows.</span></span> <span data-ttu-id="d69ed-139">例如，控制項通常會處理由對話方塊傳送的 [**WM \_ GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) 訊息，以指示對話方塊以指定的方式處理鍵盤輸入。</span><span class="sxs-lookup"><span data-stu-id="d69ed-139">For example, controls often process the [**WM\_GETDLGCODE**](/windows/desktop/dlgbox/wm-getdlgcode) message sent by dialog boxes to direct a dialog box to process keyboard input in a given way.</span></span>

<span data-ttu-id="d69ed-140">如果訊息影響控制項的操作，則應用程式定義控制項的視窗程式應處理下表中任何預先定義的控制訊息。</span><span class="sxs-lookup"><span data-stu-id="d69ed-140">The window procedure for an application-defined control should process any predefined control message in the following table if the message affects the operation of the control.</span></span>



| <span data-ttu-id="d69ed-141">訊息</span><span class="sxs-lookup"><span data-stu-id="d69ed-141">Message</span></span>                                          | <span data-ttu-id="d69ed-142">建議</span><span class="sxs-lookup"><span data-stu-id="d69ed-142">Recommendation</span></span>                                                                                                                                                                                                                                  |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d69ed-143">**WM \_ GETDLGCODE**</span><span class="sxs-lookup"><span data-stu-id="d69ed-143">**WM\_GETDLGCODE**</span></span>](/windows/desktop/dlgbox/wm-getdlgcode)       | <span data-ttu-id="d69ed-144">如果控制項使用 ENTER、ESC、TAB 或方向鍵，則為進程。</span><span class="sxs-lookup"><span data-stu-id="d69ed-144">Process if the control uses the ENTER, ESC, TAB, or arrow keys.</span></span> <span data-ttu-id="d69ed-145">[**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea)函式會將此訊息傳送給對話方塊中的控制項，以判斷是否要處理索引鍵或將它們傳遞給控制項。</span><span class="sxs-lookup"><span data-stu-id="d69ed-145">The [**IsDialogMessage**](/windows/desktop/api/winuser/nf-winuser-isdialogmessagea) function sends this message to controls in a dialog box to determine whether to process the keys or pass them to the control.</span></span> |
| [<span data-ttu-id="d69ed-146">**WM \_ GETFONT**</span><span class="sxs-lookup"><span data-stu-id="d69ed-146">**WM\_GETFONT**</span></span>](/windows/desktop/winmsg/wm-getfont)             | <span data-ttu-id="d69ed-147">如果同時處理了 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息，則為進程。</span><span class="sxs-lookup"><span data-stu-id="d69ed-147">Process if the [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message is also processed.</span></span>                                                                                                                                                                  |
| [<span data-ttu-id="d69ed-148">**WM \_ GETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d69ed-148">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)             | <span data-ttu-id="d69ed-149">如果控制項文字與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數所指定的標題不同，則為進程。</span><span class="sxs-lookup"><span data-stu-id="d69ed-149">Process if the control text is not the same as the title specified by the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>                                                                                                                 |
| [<span data-ttu-id="d69ed-150">**WM \_ GETTEXTLENGTH**</span><span class="sxs-lookup"><span data-stu-id="d69ed-150">**WM\_GETTEXTLENGTH**</span></span>](/windows/desktop/winmsg/wm-gettextlength) | <span data-ttu-id="d69ed-151">如果控制項文字與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數所指定的標題不同，則為進程。</span><span class="sxs-lookup"><span data-stu-id="d69ed-151">Process if the control text is not the same as the title specified by the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>                                                                                                                 |
| [<span data-ttu-id="d69ed-152">**WM \_ KILLFOCUS**</span><span class="sxs-lookup"><span data-stu-id="d69ed-152">**WM\_KILLFOCUS**</span></span>](/windows/desktop/inputdev/wm-killfocus)       | <span data-ttu-id="d69ed-153">如果控制項顯示插入號、焦點矩形或另一個專案，表示它有輸入焦點，則為 [進程]。</span><span class="sxs-lookup"><span data-stu-id="d69ed-153">Process if the control displays a caret, a focus rectangle, or another item to indicate that it has the input focus.</span></span>                                                                                                                            |
| [<span data-ttu-id="d69ed-154">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="d69ed-154">**WM\_SETFOCUS**</span></span>](/windows/desktop/inputdev/wm-setfocus)         | <span data-ttu-id="d69ed-155">如果控制項顯示插入號、焦點矩形或另一個專案，表示它有輸入焦點，則為 [進程]。</span><span class="sxs-lookup"><span data-stu-id="d69ed-155">Process if the control displays a caret, a focus rectangle, or another item to indicate that it has the input focus.</span></span>                                                                                                                            |
| [<span data-ttu-id="d69ed-156">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="d69ed-156">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)             | <span data-ttu-id="d69ed-157">如果控制項文字與 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函數所指定的標題不同，則為進程。</span><span class="sxs-lookup"><span data-stu-id="d69ed-157">Process if the control text is not the same as the title specified by the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function.</span></span>                                                                                                                 |
| [<span data-ttu-id="d69ed-158">**WM \_ SETFONT**</span><span class="sxs-lookup"><span data-stu-id="d69ed-158">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)             | <span data-ttu-id="d69ed-159">如果控制項顯示文字，則為進程。</span><span class="sxs-lookup"><span data-stu-id="d69ed-159">Process if the control displays text.</span></span> <span data-ttu-id="d69ed-160">當您建立具有 DS SETFONT 樣式的對話方塊時，系統會傳送此訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d69ed-160">The system sends this message when creating a dialog box that has the DS\_SETFONT style.</span></span>                                                                                                                  |



 

<span data-ttu-id="d69ed-161">應用程式定義的控制項訊息是特定的控制項，而且必須使用 [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) 或 [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) 函式明確地傳送給控制項。</span><span class="sxs-lookup"><span data-stu-id="d69ed-161">Application-defined control messages are specific to the given control and must be explicitly sent to the control by using a [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) function.</span></span> <span data-ttu-id="d69ed-162">每個訊息的數值都必須是唯一的，且不能與其他視窗訊息的值衝突。</span><span class="sxs-lookup"><span data-stu-id="d69ed-162">The numeric value for each message must be unique and must not conflict with the values of other window messages.</span></span> <span data-ttu-id="d69ed-163">為了確保應用程式定義的訊息值不會衝突，應用程式應該將唯一的數位新增至 [**WM \_ 使用者**](/windows/desktop/winmsg/wm-user) 值，以建立每個值。</span><span class="sxs-lookup"><span data-stu-id="d69ed-163">To ensure that application-defined message values do not conflict, an application should create each value by adding a unique number to the [**WM\_USER**](/windows/desktop/winmsg/wm-user) value.</span></span>

## <a name="sending-notifications-from-a-control"></a><span data-ttu-id="d69ed-164">從控制項傳送通知</span><span class="sxs-lookup"><span data-stu-id="d69ed-164">Sending Notifications from a Control</span></span>

<span data-ttu-id="d69ed-165">可能需要自訂控制項才能將事件通知傳送至父視窗，讓主應用程式可以回應這些事件。</span><span class="sxs-lookup"><span data-stu-id="d69ed-165">Custom controls might be required to send notifications of events to the parent window so that the host application can respond to these events.</span></span> <span data-ttu-id="d69ed-166">例如，自訂清單視圖可能會在使用者選取專案時傳送通知，而當按兩下專案時，可能會傳送另一則通知。</span><span class="sxs-lookup"><span data-stu-id="d69ed-166">For example, a custom list view might send a notification when the user selects an item, and another notification when an item is double-clicked.</span></span>

<span data-ttu-id="d69ed-167">通知會以 [**wm \_ 命令**](/windows/desktop/menurc/wm-command) 或 [**wm \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="d69ed-167">Notifications are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="d69ed-168">**WM \_通知** 訊息會包含超過 **WM \_ 命令** 訊息的資訊。</span><span class="sxs-lookup"><span data-stu-id="d69ed-168">**WM\_NOTIFY** messages carry more information than **WM\_COMMAND** messages.</span></span>

<span data-ttu-id="d69ed-169">控制項識別碼是應用程式用來識別傳送訊息之控制項的唯一數位。</span><span class="sxs-lookup"><span data-stu-id="d69ed-169">The control identifier is a unique number the application uses to identify the control sending the message.</span></span> <span data-ttu-id="d69ed-170">應用程式會在建立控制項時，設定控制項的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d69ed-170">The application sets the identifier for a control when it creates the control.</span></span> <span data-ttu-id="d69ed-171">應用程式會在 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函數的 *HMenu* 參數或 [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex)結構的 **id** 成員中指定識別碼。</span><span class="sxs-lookup"><span data-stu-id="d69ed-171">The application specifies the identifier either in the *hMenu* parameter of the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or in the **id** member of the [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) structure.</span></span>

<span data-ttu-id="d69ed-172">因為控制項本身不會設定控制項識別碼，所以控制項必須先取得識別碼，然後才能傳送通知訊息。</span><span class="sxs-lookup"><span data-stu-id="d69ed-172">Because the control itself does not set the control identifier, the control must retrieve the identifier before it can send notification messages.</span></span> <span data-ttu-id="d69ed-173">控制項必須使用 [**GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) 函式來取出其本身的控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="d69ed-173">A control must use the [**GetDlgCtrlID**](/windows/desktop/api/winuser/nf-winuser-getdlgctrlid) function to retrieve its own control identifier.</span></span> <span data-ttu-id="d69ed-174">雖然控制項識別碼是在控制項建立時指定為功能表控制碼，但無法使用 [**GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) 函式來取得識別碼。</span><span class="sxs-lookup"><span data-stu-id="d69ed-174">Although the control identifier is specified as the menu handle when the control is created, the [**GetMenu**](/windows/desktop/api/winuser/nf-winuser-getmenu) function cannot be used to retrieve the identifier.</span></span> <span data-ttu-id="d69ed-175">或者，當處理 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create)訊息時，控制項可以從 [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)結構中的 **hMenu** 成員取得識別碼。</span><span class="sxs-lookup"><span data-stu-id="d69ed-175">Alternatively, a control can retrieve the identifier from the **hMenu** member in the [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) structure while processing the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message.</span></span>

<span data-ttu-id="d69ed-176">下列範例，其中 *hwndControl* 是控制視窗的控制碼，而 CN \_ VALUECHANGED 是自訂通知定義，會顯示傳送控制項特定通知的兩種方式。</span><span class="sxs-lookup"><span data-stu-id="d69ed-176">The following examples, where *hwndControl* is the handle of the control window and CN\_VALUECHANGED is a custom notification definition, show the two ways of sending a control-specific notification.</span></span>


```
 // Send as WM_COMMAND.
SendMessage(GetParent(hwndControl), 
    WM_COMMAND,
    MAKEWPARAM(GetDlgCtrlID(hwndControl), CN_VALUECHANGED),
    (LPARAM)hwndControl);

// Send as WM_NOTIFY.           
NMHDR nmh;
nmh.code = CN_VALUECHANGED;
nmh.idFrom = GetDlgCtrlID(hwndControl);
nmh.hwndFrom = hwndControl;
SendMessage(GetParent(hwndControl), 
    WM_NOTIFY, 
    (WPARAM)hwndControl, 
    (LPARAM)&nmh);
```



<span data-ttu-id="d69ed-177">請注意， [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構可以是包含其他資訊之大型控制項定義結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="d69ed-177">Note that the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure can be part of a larger control-defined structure that contains additional information.</span></span> <span data-ttu-id="d69ed-178">在此範例中，控制項的舊值和新值可能包含在此結構中。</span><span class="sxs-lookup"><span data-stu-id="d69ed-178">In the example, the old and new values of the control might be contained in this structure.</span></span> <span data-ttu-id="d69ed-179"> (這類擴充結構用於許多標準通知;例如，請參閱使用 [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的 [LVN \_ INSERTITEM](lvn-insertitem.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="d69ed-179">(Such extended structures are used with many standard notifications; for example, see [LVN\_INSERTITEM](lvn-insertitem.md), which uses the [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.)</span></span>

## <a name="accessibility"></a><span data-ttu-id="d69ed-180">協助工具選項</span><span class="sxs-lookup"><span data-stu-id="d69ed-180">Accessibility</span></span>

<span data-ttu-id="d69ed-181">所有的通用控制項都支援 Microsoft Active Accessibility (MSAA) ，可讓您以程式設計方式存取螢幕讀取器之類的可存取技術應用程式。</span><span class="sxs-lookup"><span data-stu-id="d69ed-181">All the common controls support Microsoft Active Accessibility (MSAA), which enables programmatic access by accessible-technology applications such as screen-readers.</span></span> <span data-ttu-id="d69ed-182">MSAA 也可讓消費者介面自動化（較新的技術）與控制項互動。</span><span class="sxs-lookup"><span data-stu-id="d69ed-182">MSAA also enables UI Automation, a newer technology, to interact with controls.</span></span>

<span data-ttu-id="d69ed-183">自訂控制項應該執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面 (，以支援 MSAA) 或消費者介面自動化介面，或兩者都支援。</span><span class="sxs-lookup"><span data-stu-id="d69ed-183">Custom controls should implement either the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface (to support MSAA) or the UI Automation interfaces, or both.</span></span> <span data-ttu-id="d69ed-184">否則，可存取的技術產品將只能取得控制項視窗的極有限資訊、無法存取控制項的屬性，而且將無法在控制項中觸發事件。</span><span class="sxs-lookup"><span data-stu-id="d69ed-184">Otherwise, accessible-technology products will be able to obtain only very limited information about the control window, will not have access to the control's properties, and will be unable to trigger events in the control.</span></span>

<span data-ttu-id="d69ed-185">如需讓控制項可供存取的詳細資訊，請參閱 [Windows AUTOMATION API](/windows/desktop/WinAuto/windows-automation-api-portal)。</span><span class="sxs-lookup"><span data-stu-id="d69ed-185">For more information about making your control accessible, see [Windows Automation API](/windows/desktop/WinAuto/windows-automation-api-portal).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d69ed-186">相關主題</span><span class="sxs-lookup"><span data-stu-id="d69ed-186">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d69ed-187">**概念**</span><span class="sxs-lookup"><span data-stu-id="d69ed-187">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d69ed-188">一般控制項參考</span><span class="sxs-lookup"><span data-stu-id="d69ed-188">General Control Reference</span></span>](common-control-reference.md)
</dt> <dt>

[<span data-ttu-id="d69ed-189">使用自訂繪圖自訂控制項的外觀</span><span class="sxs-lookup"><span data-stu-id="d69ed-189">Customizing a Control's Appearance Using Custom Draw</span></span>](custom-draw.md)
</dt> <dt>

[<span data-ttu-id="d69ed-190">控制訊息</span><span class="sxs-lookup"><span data-stu-id="d69ed-190">Control Messages</span></span>](control-messages.md)
</dt> <dt>

[<span data-ttu-id="d69ed-191">搭配 Owner-Drawn 控制項使用視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="d69ed-191">Using Visual Styles with Owner-Drawn Controls</span></span>](using-visual-styles.md)
</dt> </dl>

 

 