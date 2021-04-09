---
title: 如何建立 Owner-Drawn 下拉式方塊
description: 本主題將示範如何使用主控描繪的下拉式方塊。
ms.assetid: D866DE82-9734-4E8A-A366-5870C25B7C7B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5355dd33fe0067165308e9e6e5885b76edbe7ceb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024127"
---
# <a name="how-to-create-an-owner-drawn-combo-box"></a><span data-ttu-id="31563-103">如何建立 Owner-Drawn 下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="31563-103">How to Create an Owner-Drawn Combo Box</span></span>

<span data-ttu-id="31563-104">本主題將示範如何使用主控描繪的下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="31563-104">This topic demonstrates how to use an owner-drawn combo box.</span></span> <span data-ttu-id="31563-105">C + + 程式碼範例會使用主控描繪的下拉式清單方塊，顯示四個食物群組，每個都以點陣圖和名稱表示。</span><span class="sxs-lookup"><span data-stu-id="31563-105">The C++ code example uses an owner-drawn drop-down list box to display the four food groups, each represented by a bitmap and a name.</span></span> <span data-ttu-id="31563-106">選取食物群組會導致該群組中的食物出現在清單中。</span><span class="sxs-lookup"><span data-stu-id="31563-106">Selecting a food group causes the foods in that group to appear in a list.</span></span>

![顯示對話方塊的螢幕擷取畫面，其中包含清單方塊和展開的下拉式清單方塊，其中顯示每個專案的圖示和標籤](images/cscbx-01.png)

<span data-ttu-id="31563-108">對話方塊也包含 (IDLIST.TXT) 的清單方塊和兩個按鈕： **[確定]** (IDOK) 和 [ **取消** ] (IDCANCEL) 。</span><span class="sxs-lookup"><span data-stu-id="31563-108">The dialog box also contains a list box (IDLIST) and two buttons: **OK** (IDOK) and **Cancel** (IDCANCEL).</span></span> <span data-ttu-id="31563-109">IDOK 和 IDCANCEL 常數是由 SDK 標頭檔所定義。</span><span class="sxs-lookup"><span data-stu-id="31563-109">The IDOK and IDCANCEL constants are defined by the SDK header files.</span></span> <span data-ttu-id="31563-110">常數 IDLIST.TXT 會定義在應用程式的標頭檔中，就像控制項識別碼 IDCOMBO 一樣。</span><span class="sxs-lookup"><span data-stu-id="31563-110">The constant IDLIST is defined in the application's header file, as is the control identifier, IDCOMBO.</span></span> <span data-ttu-id="31563-111">如需對話方塊的詳細資訊，請參閱 [對話方塊](/windows/desktop/dlgbox/dialog-boxes)。</span><span class="sxs-lookup"><span data-stu-id="31563-111">For more information about dialog boxes, see [Dialog Boxes](/windows/desktop/dlgbox/dialog-boxes).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="31563-112">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="31563-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="31563-113">技術</span><span class="sxs-lookup"><span data-stu-id="31563-113">Technologies</span></span>

-   [<span data-ttu-id="31563-114">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="31563-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="31563-115">必要條件</span><span class="sxs-lookup"><span data-stu-id="31563-115">Prerequisites</span></span>

-   <span data-ttu-id="31563-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="31563-116">C/C++</span></span>
-   <span data-ttu-id="31563-117">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="31563-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="31563-118">指示</span><span class="sxs-lookup"><span data-stu-id="31563-118">Instructions</span></span>

### <a name="step-1-create-the-owner-drawn-dialog-box"></a><span data-ttu-id="31563-119">步驟1：建立 Owner-Drawn 對話方塊</span><span class="sxs-lookup"><span data-stu-id="31563-119">Step 1: Create the Owner-Drawn Dialog Box</span></span>

<span data-ttu-id="31563-120">程式碼範例會使用 [**對話方塊**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) 函數來建立強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="31563-120">The code example uses the [**DialogBox**](/windows/desktop/api/winuser/nf-winuser-dialogboxa) function to create a modal dialog box.</span></span> <span data-ttu-id="31563-121">對話方塊範本 [IDD SQMEAL] 會 \_ 定義下拉式方塊的視窗樣式、按鈕和控制項識別碼。</span><span class="sxs-lookup"><span data-stu-id="31563-121">The dialog box template, IDD\_SQMEAL, defines the window styles, buttons, and control identifiers for the combo box.</span></span> <span data-ttu-id="31563-122">此範例中的下拉式方塊會使用 [**cbs \_ DROPDOWNLIST**](combo-box-styles.md)、 [**cbs \_ OWNERDRAWFIXED**](combo-box-styles.md)、 [**cbs \_ SORT**](combo-box-styles.md)、 [**cbs \_ HASSTRINGS**](combo-box-styles.md)、 [**ws \_ VSCROLL**](/windows/desktop/winmsg/window-styles)和 [**ws \_ TABSTOP**](/windows/desktop/winmsg/window-styles) 樣式。</span><span class="sxs-lookup"><span data-stu-id="31563-122">The combo box in this example uses the [**CBS\_DROPDOWNLIST**](combo-box-styles.md), [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md), [**CBS\_SORT**](combo-box-styles.md), [**CBS\_HASSTRINGS**](combo-box-styles.md), [**WS\_VSCROLL**](/windows/desktop/winmsg/window-styles), and [**WS\_TABSTOP**](/windows/desktop/winmsg/window-styles) styles.</span></span>


```C++
DialogBox(hInst, MAKEINTRESOURCE(IDD_SQMEAL), 
    hWnd, FoodDlgProc);
```



### <a name="step-2-process-the-wm_initdialog-and-wm_destroy-messages-in-a-dialog-box"></a><span data-ttu-id="31563-123">步驟2： \_ 在對話方塊中處理 wm INITDIALOG 和 wm \_ 摧毀訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-123">Step 2: Process the WM\_INITDIALOG and WM\_DESTROY messages in a dialog box.</span></span>

<span data-ttu-id="31563-124">當您在對話方塊中使用下拉式方塊時，通常會藉由初始化下拉式方塊來回應 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-124">When you use a combo box in a dialog box, you usually respond to a [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message by initializing the combo box.</span></span> <span data-ttu-id="31563-125">應用程式會載入用於主控描繪下拉式方塊的點陣圖，然後呼叫應用程式定義的函式 `InitGroupList` 來初始化下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="31563-125">The application loads the bitmaps used for the owner-drawn combo box and then calls the application-defined `InitGroupList` function to initialize the combo box.</span></span> <span data-ttu-id="31563-126">它也會選取下拉式方塊中的第一個清單專案，然後呼叫應用程式定義的函式 `InitFoodList` 來初始化清單方塊。</span><span class="sxs-lookup"><span data-stu-id="31563-126">It also selects the first list item in the combo box and then calls the application-defined `InitFoodList` function to initialize the list box.</span></span>

<span data-ttu-id="31563-127">在此範例中，主控描繪下拉式方塊是一個下拉式清單方塊，其中包含四個食物群組的每個名稱。</span><span class="sxs-lookup"><span data-stu-id="31563-127">In the example, the owner-drawn combo box is a drop-down list box that contains the names of each of the four food groups.</span></span> <span data-ttu-id="31563-128">`InitGroupList` 新增每個食物群組的名稱，並使用 [**CB \_ SETITEMDATA**](cb-setitemdata.md) 訊息，將點陣圖控制碼與識別食物群組的每個清單專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="31563-128">`InitGroupList` adds the name of each food group , and uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item that identifies a food group.</span></span>

<span data-ttu-id="31563-129">範例中的清單方塊包含所選食物群組中食物的名稱。</span><span class="sxs-lookup"><span data-stu-id="31563-129">The list box in the example contains the names of foods in the selected food group.</span></span> <span data-ttu-id="31563-130">**InitFoodList** 會重設清單方塊的內容，然後在 [目前食物群組] 下拉式清單方塊中加入目前食物選取專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="31563-130">**InitFoodList** resets the contents of the list box, then adds the names of the current food selection in the current food group drop-down list box.</span></span>


```C++
case WM_INITDIALOG:

    // Call an application-defined function to load bitmap resources.
    if (!LoadIconBitmaps())
    {
        EndDialog(hDlg, -1);
        break;
    }

    // Initialize the food groups combo box and select the first item.
    InitGroupList(hDlg);
    SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

    // Initialize the food list box and select the first item.
    InitFoodList(hDlg);
    SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

     return (INT_PTR)TRUE;
```



<span data-ttu-id="31563-131">當它收到 [**WM 終結 \_**](/windows/desktop/winmsg/wm-destroy) 訊息時，應用程式會刪除主控描繪下拉式方塊中的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="31563-131">When it receives the [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message, the application deletes the bitmaps in the owner-drawn combo box.</span></span>


```C++
case WM_DESTROY:

    // Call the application-defined function to free the bitmap resources.
    DeleteIconBitmaps();
    break;
```



### <a name="step-3-process-the-wm_measureitem-message"></a><span data-ttu-id="31563-132">步驟3：處理 WM \_ MEASUREITEM 訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-132">Step 3: Process the WM\_MEASUREITEM message.</span></span>

<span data-ttu-id="31563-133">主控描繪的下拉式列示方塊會將 [**WM \_ MEASUREITEM**](wm-measureitem.md) 訊息傳送至其父視窗或對話方塊程式，讓應用程式可以設定每個清單專案的維度。</span><span class="sxs-lookup"><span data-stu-id="31563-133">An owner-drawn combo box sends the [**WM\_MEASUREITEM**](wm-measureitem.md) message to its parent window or dialog box procedure so that the application can set the dimensions of each list item.</span></span> <span data-ttu-id="31563-134">因為範例下拉式列示方塊具有 [**CBS \_ OWNERDRAWFIXED**](combo-box-styles.md) 樣式，所以系統只會傳送一次 **WM \_ MEASUREITEM** 訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-134">Because the example combo box has the [**CBS\_OWNERDRAWFIXED**](combo-box-styles.md) style, the system sends the **WM\_MEASUREITEM** message only once.</span></span> <span data-ttu-id="31563-135">具有 [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) 樣式的下拉式方塊會為每個清單專案傳送 **WM \_ MEASUREITEM** 訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-135">Combo boxes with the [**CBS\_OWNERDRAWVARIABLE**](combo-box-styles.md) style send a **WM\_MEASUREITEM** message for each list item.</span></span>

<span data-ttu-id="31563-136">*LParam* 參數是 [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)結構的指標，可識別控制項和清單專案。</span><span class="sxs-lookup"><span data-stu-id="31563-136">The *lParam* parameter is a pointer to a [**MEASUREITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="31563-137">它也包含清單專案的預設維度。</span><span class="sxs-lookup"><span data-stu-id="31563-137">It also contains the default dimensions of the list item.</span></span> <span data-ttu-id="31563-138">此範例會修改 **itemHeight** 結構成員，以確保清單專案夠高，足以容納食物群組點陣圖。</span><span class="sxs-lookup"><span data-stu-id="31563-138">The example modifies the **itemHeight** structure member to ensure that the list items are high enough to accommodate the food-group bitmaps.</span></span>


```C++
case WM_MEASUREITEM:
    {
    // Set the height of the items in the food groups combo box.
    LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

    if (lpmis->itemHeight < CY_BITMAP + 2)
        lpmis->itemHeight = CY_BITMAP + 2;

    break;
    }
```



### <a name="step-4-process-the-wm_drawitem-message"></a><span data-ttu-id="31563-139">步驟4：處理 WM \_ DRAWITEM 訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-139">Step 4: Process the WM\_DRAWITEM message.</span></span>

<span data-ttu-id="31563-140">擁有者繪製的下拉式方塊會在每次應用程式必須重新繪製清單專案時，將 [**WM \_ DRAWITEM**](wm-drawitem.md) 訊息傳送至其父視窗或對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="31563-140">An owner-drawn combo box sends the [**WM\_DRAWITEM**](wm-drawitem.md) message to its parent window or dialog box procedure each time the application must repaint a list item.</span></span> <span data-ttu-id="31563-141">*LParam* 參數是 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的指標，可識別控制項和清單專案。</span><span class="sxs-lookup"><span data-stu-id="31563-141">The *lParam* parameter is a pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure that identifies the control and list item.</span></span> <span data-ttu-id="31563-142">它也包含繪製專案所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="31563-142">It also contains information needed to paint the item.</span></span>

<span data-ttu-id="31563-143">範例應用程式會顯示清單專案文字，以及與食物群組相關聯的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="31563-143">The example application displays the list-item text and the bitmap associated with the food group.</span></span> <span data-ttu-id="31563-144">如果專案具有焦點，則也會繪製焦點矩形。</span><span class="sxs-lookup"><span data-stu-id="31563-144">If the item has the focus, it also draws a focus rectangle.</span></span> <span data-ttu-id="31563-145">在顯示文字之前，範例會根據選取的專案來設定前景和背景色彩。</span><span class="sxs-lookup"><span data-stu-id="31563-145">Before displaying the text, the example sets the foreground and background colors, based on the item selected.</span></span> <span data-ttu-id="31563-146">因為下拉式方塊具有 [**CBS \_ HASSTRINGS**](combo-box-styles.md) 樣式，所以下拉式方塊會維護每個可使用 [**CB \_ GETLBTEXT**](cb-getlbtext.md) 訊息抓取之清單專案的文字。</span><span class="sxs-lookup"><span data-stu-id="31563-146">Because the combo box has the [**CBS\_HASSTRINGS**](combo-box-styles.md) style, the combo box maintains the text for each list item that can be retrieved using the [**CB\_GETLBTEXT**](cb-getlbtext.md) message.</span></span>

<span data-ttu-id="31563-147">用於清單專案的點陣圖取決於食物群組。</span><span class="sxs-lookup"><span data-stu-id="31563-147">The bitmaps used for the list item depend on the food group.</span></span> <span data-ttu-id="31563-148">`InitGroupList` 使用 [**CB \_ SETITEMDATA**](cb-setitemdata.md) 訊息，將點陣圖控制碼與每個清單專案產生關聯。</span><span class="sxs-lookup"><span data-stu-id="31563-148">`InitGroupList` uses the [**CB\_SETITEMDATA**](cb-setitemdata.md) message to associate a bitmap handle with each list item.</span></span> <span data-ttu-id="31563-149">視窗程式會從 [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)結構的 **itemData** 成員抓取點陣圖控制碼。</span><span class="sxs-lookup"><span data-stu-id="31563-149">The window procedure retrieves the bitmap handle from the **itemData** member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure.</span></span> <span data-ttu-id="31563-150">系統會為每個食物群組符號使用兩個位圖：具有 SRCAND 點陣運算的單色點陣圖，可清除影像後方的不規則區域，以及具有 SRCPAINT 點陣作業來繪製影像的色彩點陣圖。</span><span class="sxs-lookup"><span data-stu-id="31563-150">The system uses two bitmaps for each food group symbol: a monochrome bitmap with the SRCAND raster operation to erase the irregular region behind the image, and a color bitmap with the SRCPAINT raster operation to paint the image.</span></span>


```C++
case WM_DRAWITEM:
    {
    COLORREF clrBackground;
    COLORREF clrForeground;
    TEXTMETRIC tm;
    int x;
    int y;
    HRESULT hr;
    size_t cch;

    LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
       
    if (lpdis->itemID == -1) // Empty item)
        break;

    // Get the food icon from the item data.
    hbmIcon = (HBITMAP) lpdis->itemData;

    // The colors depend on whether the item is selected.
    clrForeground = SetTextColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

    clrBackground = SetBkColor(lpdis->hDC, 
        GetSysColor(lpdis->itemState & ODS_SELECTED ?
        COLOR_HIGHLIGHT : COLOR_WINDOW));

    // Calculate the vertical and horizontal position.
    GetTextMetrics(lpdis->hDC, &tm);
    y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
    x = LOWORD(GetDialogBaseUnits()) / 4;

    // Get and display the text for the list item.
    SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
        lpdis->itemID, (LPARAM) achTemp);

    hr = StringCchLength(achTemp, 256, &cch);
    if (FAILED(hr))
    {
        // TODO: Write error handler.
    }

    ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
        ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
        achTemp, (UINT)cch, NULL);

    // Restore the previous colors.
    SetTextColor(lpdis->hDC, clrForeground);
    SetBkColor(lpdis->hDC, clrBackground);
    
    //  Draw the food icon for the item. 
    HDC hdc = CreateCompatibleDC(lpdis->hDC); 
    if (hdc == NULL) 
        break; 
 
    SelectObject(hdc, hbmMask); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
    SelectObject(hdc, hbmIcon); 
    BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
        CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
    DeleteDC(hdc); 
  
    // If the item has the focus, draw the focus rectangle.
    if (lpdis->itemState & ODS_FOCUS)
        DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

    break;
    }
```



### <a name="step-5-process-the-wm_command-message"></a><span data-ttu-id="31563-151">步驟5：處理 WM \_ 命令訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-151">Step 5: Process the WM\_COMMAND message.</span></span>

<span data-ttu-id="31563-152">當對話方塊控制項中發生事件時，控制項會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息來通知對話方塊程式。</span><span class="sxs-lookup"><span data-stu-id="31563-152">When an event occurs in a dialog box control, the control notifies the dialog box procedure by means of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span> <span data-ttu-id="31563-153">此範例會從下拉式方塊、清單方塊和 [ **確定]** 按鈕處理通知訊息。</span><span class="sxs-lookup"><span data-stu-id="31563-153">The example processes notification messages from the combo box, the list box, and the **OK** button.</span></span> <span data-ttu-id="31563-154">控制項識別碼是 *wParam* 的低序位字組，而通知碼是 *wParam* 的高序位字。</span><span class="sxs-lookup"><span data-stu-id="31563-154">The control identifier is in the low-order word of *wParam*, and the notification code is in the high-order word of *wParam*.</span></span>

<span data-ttu-id="31563-155">如果控制項識別碼是 IDCOMBO，則下拉式方塊中已發生事件。</span><span class="sxs-lookup"><span data-stu-id="31563-155">If the control identifier is IDCOMBO, an event has occurred in the combo box.</span></span> <span data-ttu-id="31563-156">在 [回應] 中，對話方塊程式會略過 [**CBN \_ SELENDOK**](cbn-selendok.md)以外的所有其他下拉式方塊事件（表示已進行選取、關閉下拉式清單方塊），以及應接受變更。</span><span class="sxs-lookup"><span data-stu-id="31563-156">In response, the dialog box procedure ignores all other combo box events except [**CBN\_SELENDOK**](cbn-selendok.md), which indicates that a selection was made, the drop down list box was closed, and the changes made should be accepted.</span></span> <span data-ttu-id="31563-157">對話方塊程式會呼叫 `InitFoodList` ，以重設清單方塊的內容，並在下拉式清單方塊中加入目前選取專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="31563-157">The dialog box procedure calls `InitFoodList` to reset the contents of the list box and to add the names of the current selections in the drop-down list box.</span></span>

<span data-ttu-id="31563-158">如果控制項識別碼是 IDLIST.TXT，清單方塊中就會發生事件。</span><span class="sxs-lookup"><span data-stu-id="31563-158">If the control identifier is IDLIST, an event has occurred in the list box.</span></span> <span data-ttu-id="31563-159">這會導致對話方塊程式忽略所有清單方塊事件（ [**LBN \_ DBLCLK**](lbn-dblclk.md)除外），這表示使用者已按兩下清單專案。</span><span class="sxs-lookup"><span data-stu-id="31563-159">This causes the dialog box procedure to ignore all list box events except [**LBN\_DBLCLK**](lbn-dblclk.md), which indicates that the user has double-clicked a list item.</span></span> <span data-ttu-id="31563-160">此事件的處理方式就如同已選擇 **[確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="31563-160">This event is processed in the same way as if an **OK** button had been chosen.</span></span>

<span data-ttu-id="31563-161">如果控制項識別碼是 IDOK，則使用者已選擇 [ **確定]** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="31563-161">If the control identifier is IDOK, the user has chosen the **OK** button.</span></span> <span data-ttu-id="31563-162">在 [回應] 中，對話方塊程式會將所選食物的名稱插入應用程式的多行編輯控制項中，然後呼叫 [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) 函式來關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="31563-162">In response, the dialog box procedure inserts the name of the selected food into the application's multi-line edit control, then calls the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function to close the dialog box.</span></span>

<span data-ttu-id="31563-163">如果控制項識別碼是 IDCANCEL，則使用者已按一下 [ **取消** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="31563-163">If the control identifier is IDCANCEL, the user has clicked the **Cancel** button.</span></span> <span data-ttu-id="31563-164">在 [回應] 中，對話方塊程式會呼叫 [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) 來關閉對話方塊。</span><span class="sxs-lookup"><span data-stu-id="31563-164">In response, the dialog box procedure calls [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) to close the dialog box.</span></span>


```C++
case WM_COMMAND:
        switch (LOWORD(wParam)) 
        { 
            case IDCOMBO: 
                if (HIWORD(wParam) == CBN_SELENDOK) 
                { 
                    InitFoodList(hDlg); 
                    SendDlgItemMessage(hDlg, IDLIST, 
                        LB_SETCURSEL, 0, 0); 
                } 
                break; 
 
            case IDLIST: 
                if (HIWORD(wParam) != LBN_DBLCLK) 
                    break; 
 
            // For a double-click, process the OK case. 
            case IDOK: 
 
                // Get the text for the selected list item. 
                hwnd = GetDlgItem(hDlg, IDLIST); 

                // Here it is assumed the text can fit into achTemp.
                // If there is doubt, call LB_GETTEXTLENGTH first.
                SendMessage(hwnd, LB_GETTEXT, 
                    SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                    (LPARAM) achTemp); 
 
                // TODO: Do something with the selected text.
 
                EndDialog(hDlg, 0); 
                break; 
 
            case IDCANCEL: 
                hwnd = GetDlgItem(hDlg, IDCOMBO); 
                if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                    SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                else EndDialog(hDlg, 0); 
        } 
        break; 
```



## <a name="complete-example"></a><span data-ttu-id="31563-165">完整範例</span><span class="sxs-lookup"><span data-stu-id="31563-165">Complete example</span></span>

<span data-ttu-id="31563-166">以下是 [ **方形飲食** ] 對話方塊的對話方塊程式和支援功能。</span><span class="sxs-lookup"><span data-stu-id="31563-166">Following is the dialog box procedure and the supporting functions for the **Square Meal** dialog box.</span></span>


```C++
#define ID_BREAD 0
#define ID_DAIRY 1
#define ID_FRUIT 2
#define ID_MEAT  3

#define CX_BITMAP 24
#define CY_BITMAP 24

HBITMAP hbmBread;
HBITMAP hbmDairy;
HBITMAP hbmMeat;
HBITMAP hbmFruit;
HBITMAP hbmMask;

HBITMAP hbmIcon;
```

```C++
// Message handler for Square Meal dialog box.
INT_PTR CALLBACK FoodDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam)
{
    UNREFERENCED_PARAMETER(lParam);
    TCHAR achTemp[256];
    HWND hwnd;

    switch (message)
    {
    case WM_INITDIALOG:

        // Call an application-defined function to load bitmap resources.
        if (!LoadIconBitmaps())
        {
            EndDialog(hDlg, -1);
            break;
        }

        // Initialize the food groups combo box and select the first item.
        InitGroupList(hDlg);
        SendDlgItemMessage(hDlg, IDCOMBO, CB_SETCURSEL, 0, 0); 

        // Initialize the food list box and select the first item.
        InitFoodList(hDlg);
        SendDlgItemMessage(hDlg, IDLIST, LB_SETCURSEL, 0, 0); 

         return (INT_PTR)TRUE;
   
    case WM_MEASUREITEM:
        {
        // Set the height of the items in the food groups combo box.
        LPMEASUREITEMSTRUCT lpmis = (LPMEASUREITEMSTRUCT) lParam;

        if (lpmis->itemHeight < CY_BITMAP + 2)
            lpmis->itemHeight = CY_BITMAP + 2;

        break;
        }

    case WM_DRAWITEM:
        {
        COLORREF clrBackground;
        COLORREF clrForeground;
        TEXTMETRIC tm;
        int x;
        int y;
        HRESULT hr;
        size_t cch;

        LPDRAWITEMSTRUCT lpdis = (LPDRAWITEMSTRUCT) lParam;
           
        if (lpdis->itemID == -1) // Empty item)
            break;

        // Get the food icon from the item data.
        hbmIcon = (HBITMAP) lpdis->itemData;

        // The colors depend on whether the item is selected.
        clrForeground = SetTextColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHTTEXT : COLOR_WINDOWTEXT));

        clrBackground = SetBkColor(lpdis->hDC, 
            GetSysColor(lpdis->itemState & ODS_SELECTED ?
            COLOR_HIGHLIGHT : COLOR_WINDOW));

        // Calculate the vertical and horizontal position.
        GetTextMetrics(lpdis->hDC, &tm);
        y = (lpdis->rcItem.bottom + lpdis->rcItem.top - tm.tmHeight) / 2;
        x = LOWORD(GetDialogBaseUnits()) / 4;

        // Get and display the text for the list item.
        SendMessage(lpdis->hwndItem, CB_GETLBTEXT,
            lpdis->itemID, (LPARAM) achTemp);

        hr = StringCchLength(achTemp, 256, &cch);
        if (FAILED(hr))
        {
            // TODO: Write error handler.
        }

        ExtTextOut(lpdis->hDC, CX_BITMAP + 2 * x, y,
            ETO_CLIPPED | ETO_OPAQUE, &lpdis->rcItem,
            achTemp, (UINT)cch, NULL);

        // Restore the previous colors.
        SetTextColor(lpdis->hDC, clrForeground);
        SetBkColor(lpdis->hDC, clrBackground);
        
        //  Draw the food icon for the item. 
        HDC hdc = CreateCompatibleDC(lpdis->hDC); 
        if (hdc == NULL) 
            break; 
 
        SelectObject(hdc, hbmMask); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCAND); 
 
        SelectObject(hdc, hbmIcon); 
        BitBlt(lpdis->hDC, x, lpdis->rcItem.top + 1, 
            CX_BITMAP, CY_BITMAP, hdc, 0, 0, SRCPAINT); 
 
        DeleteDC(hdc); 
      
        // If the item has the focus, draw the focus rectangle.
        if (lpdis->itemState & ODS_FOCUS)
            DrawFocusRect(lpdis->hDC, &lpdis->rcItem);

        break;
        }

    case WM_COMMAND:
            switch (LOWORD(wParam)) 
            { 
                case IDCOMBO: 
                    if (HIWORD(wParam) == CBN_SELENDOK) 
                    { 
                        InitFoodList(hDlg); 
                        SendDlgItemMessage(hDlg, IDLIST, 
                            LB_SETCURSEL, 0, 0); 
                    } 
                    break; 
 
                case IDLIST: 
                    if (HIWORD(wParam) != LBN_DBLCLK) 
                        break; 
 
                // For a double-click, process the OK case. 
                case IDOK: 
 
                    // Get the text for the selected list item. 
                    hwnd = GetDlgItem(hDlg, IDLIST); 

                    // Here it is assumed the text can fit into achTemp.
                    // If there is doubt, call LB_GETTEXTLENGTH first.
                    SendMessage(hwnd, LB_GETTEXT, 
                        SendMessage(hwnd, LB_GETCURSEL, 0, 0), 
                        (LPARAM) achTemp); 
 
                    // TODO: Do something with the selected text.
 
                    EndDialog(hDlg, 0); 
                    break; 
 
                case IDCANCEL: 
                    hwnd = GetDlgItem(hDlg, IDCOMBO); 
                    if (SendMessage(hwnd, CB_GETDROPPEDSTATE, 0, 0)) 
                        SendMessage(hwnd, CB_SHOWDROPDOWN, FALSE, 0); 
                    else EndDialog(hDlg, 0); 
            } 
            break; 

    case WM_DESTROY:

        // Call the application-defined function to free the bitmap resources.
        DeleteIconBitmaps();
        break;
    }
    return (INT_PTR)FALSE;
}

// Loads string resources and adds them as items to the drop-down list of
//   the food groups combo box. The bitmap handle of each item&#39;s icon is
//   stored as item data for easy access when the item needs to be drawn.
// 
void InitGroupList(HWND hDlg)
{
    TCHAR achTemp[256];
    DWORD dwIndex;

    // Get the handle of the food groups combo box.
    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);

    LoadString(hInst, IDS_BREAD, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmBread);
    
    LoadString(hInst, IDS_DAIRY, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmDairy);

    LoadString(hInst, IDS_FRUIT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmFruit); 

    LoadString(hInst, IDS_MEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR)); 
    dwIndex = SendMessage(hwndGroupsBox, CB_ADDSTRING, 0, (LPARAM) achTemp);
    SendMessage(hwndGroupsBox, CB_SETITEMDATA, dwIndex, (LPARAM) hbmMeat);

    return;
}

// Fills the food list based on the selected item in the food groups
//   combo box.
void InitFoodList(HWND hDlg)
{
    TCHAR achTemp[256];

    HWND hwndGroupsBox = GetDlgItem(hDlg, IDCOMBO);
    HWND hwndFoodList = GetDlgItem(hDlg, IDLIST);

    // Clear the list contents.
    SendMessage(hwndFoodList, LB_RESETCONTENT, 0, 0);

    // Find out which food group is selected.
    int idFoodGroup = SendMessage(hwndGroupsBox, CB_GETCURSEL, 0, 0);

    switch (idFoodGroup)
    {
    case ID_BREAD:
        LoadString(hInst, IDS_OAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_WHEAT, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_RYE, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        break;

    case ID_DAIRY:
        LoadString(hInst, IDS_CHEDDAR, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_MILK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PROCESSED, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_SWISS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);
        
        break;

    case ID_FRUIT:
        LoadString(hInst, IDS_APPLES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_BANANAS, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_ORANGES, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    case ID_MEAT:
        LoadString(hInst, IDS_BEEF, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_CHICKEN, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        LoadString(hInst, IDS_PORK, achTemp, sizeof(achTemp)/sizeof(TCHAR));
        SendMessage(hwndFoodList, LB_ADDSTRING, 0, (LPARAM) achTemp);

        break;

    default:
        break;
    }

    return;
}

// Loads the food icon bitmaps from the application resources.
//
BOOL LoadIconBitmaps(void)
{
    hbmBread = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_BREAD));

    if (hbmBread != NULL)
         hbmDairy = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_DAIRY));

    if (hbmDairy != NULL)
         hbmMeat = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MEAT));

    if (hbmMeat != NULL)
        hbmFruit = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_FRUIT));
    
    if (hbmFruit != NULL)
        hbmMask = LoadBitmap(hInst, MAKEINTRESOURCE(IDB_MASK));

    if (hbmMask != NULL)
        return TRUE;
        
    return FALSE;
}

// Frees the icon bitmps.
//
void DeleteIconBitmaps(void)
{
    FreeResource(reinterpret_cast<HGLOBAL>(hbmBread));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmDairy));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMeat));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmFruit));
    FreeResource(reinterpret_cast<HGLOBAL>(hbmMask));
}
```


## <a name="related-topics"></a><span data-ttu-id="31563-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="31563-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31563-168">使用下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="31563-168">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> </dl>

 

 