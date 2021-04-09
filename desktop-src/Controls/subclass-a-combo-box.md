---
title: 如何子類別化下拉式方塊
description: 本主題將示範如何將下拉式方塊設為子類別。
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b48301309597c53f02ca87d1d1748ab1fe05139
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024193"
---
# <a name="how-to-subclass-a-combo-box"></a><span data-ttu-id="b456f-103">如何子類別化下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="b456f-103">How to Subclass a Combo Box</span></span>

<span data-ttu-id="b456f-104">本主題將示範如何將下拉式方塊設為子類別。</span><span class="sxs-lookup"><span data-stu-id="b456f-104">This topic demonstrates how to subclass combo boxes.</span></span> <span data-ttu-id="b456f-105">C + + 範例應用程式會建立包含兩個下拉式方塊的工具列視窗。</span><span class="sxs-lookup"><span data-stu-id="b456f-105">The C++ example application creates a toolbar window that contains two combo boxes.</span></span> <span data-ttu-id="b456f-106">藉由將下拉式方塊中的編輯控制項子類別化，工具列視窗會攔截 TAB、ENTER 和 ESC 鍵（否則會忽略）。</span><span class="sxs-lookup"><span data-stu-id="b456f-106">By subclassing the edit controls within the combo boxes, the toolbar window intercepts TAB, ENTER, and ESC keys that would otherwise be ignored.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="b456f-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="b456f-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="b456f-108">技術</span><span class="sxs-lookup"><span data-stu-id="b456f-108">Technologies</span></span>

-   [<span data-ttu-id="b456f-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="b456f-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="b456f-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="b456f-110">Prerequisites</span></span>

-   <span data-ttu-id="b456f-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="b456f-111">C/C++</span></span>
-   <span data-ttu-id="b456f-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="b456f-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="b456f-113">指示</span><span class="sxs-lookup"><span data-stu-id="b456f-113">Instructions</span></span>

### <a name="process-the-wm_create-message"></a><span data-ttu-id="b456f-114">處理 WM \_ 建立訊息</span><span class="sxs-lookup"><span data-stu-id="b456f-114">Process the WM\_CREATE Message</span></span>

<span data-ttu-id="b456f-115">應用程式會處理 [**WM \_ 建立**](/windows/desktop/winmsg/wm-create) 訊息，以建立兩個下拉式方塊控制項做為子視窗。</span><span class="sxs-lookup"><span data-stu-id="b456f-115">The application processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to create two combo box controls as child windows.</span></span>


```C++
//  Create two combo box child windows. 
dwBaseUnits = GetDialogBaseUnits(); 
 
hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (6 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, NULL, NULL);  
 
hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (112 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, hInst, NULL); 
```



<span data-ttu-id="b456f-116">然後，應用程式會將編輯控制項子類別化 (選取欄位) 在每個下拉式方塊中，因為它們會接收簡單和下拉式清單方塊的字元輸入。</span><span class="sxs-lookup"><span data-stu-id="b456f-116">The application then subclasses the edit controls (selection fields) in each combo box, because they receive the character input for simple and drop-down combo box.</span></span> <span data-ttu-id="b456f-117">最後，它會呼叫 [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) 函式，以取得每個編輯控制項的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b456f-117">Finally, it calls the [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) function to retrieve the handle to each edit control.</span></span>

<span data-ttu-id="b456f-118">若要子類別化編輯控制項，應用程式會呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函式，並以應用程式定義的 **SubClassProc** 函式指標取代類別視窗程式的指標。</span><span class="sxs-lookup"><span data-stu-id="b456f-118">To subclass the edit controls, the application calls the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function, replacing the pointer to the class window procedure with a pointer to the application-defined **SubClassProc** function.</span></span> <span data-ttu-id="b456f-119">原始視窗程式的指標會儲存在全域變數 *lpfnEditWndProc* 中。</span><span class="sxs-lookup"><span data-stu-id="b456f-119">The pointer to the original window procedure is saved in the global variable *lpfnEditWndProc*.</span></span>

<span data-ttu-id="b456f-120">**SubClassProc** 會攔截索引標籤、輸入和 ESC 鍵，並藉由傳送應用程式定義的訊息 (WM 索引標籤 \_ 、WM \_ ESC 和 wm 輸入) 來通知工具列視窗 \_ 。</span><span class="sxs-lookup"><span data-stu-id="b456f-120">**SubClassProc** intercepts TAB, ENTER, and ESC keys and notifies the toolbar window by sending application-defined messages (WM\_TAB, WM\_ESC, and WM\_ENTER).</span></span> <span data-ttu-id="b456f-121">**SubClassProc** 會使用 [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) 函數，將大部分訊息傳遞至原始視窗程式 *lpfnEditWndProc*。</span><span class="sxs-lookup"><span data-stu-id="b456f-121">**SubClassProc** uses the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function to pass most messages to the original window procedure, *lpfnEditWndProc*.</span></span>


```C++
//  Get the edit window handle to each combo box. 
pt.x = 1; 
pt.y = 1; 
hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
//  Change the window procedure for both edit windows 
//  to the subclass procedure. 
lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
    GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
```



### <a name="process-the-wm_setfocus-message"></a><span data-ttu-id="b456f-122">處理 WM \_ SETFOCUS 訊息</span><span class="sxs-lookup"><span data-stu-id="b456f-122">Process the WM\_SETFOCUS Message</span></span>

<span data-ttu-id="b456f-123">當工具列視窗收到輸入焦點時，會立即將焦點設定為工具列中的第一個下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="b456f-123">When the toolbar window receives the input focus, it immediately sets the focus to the first combo box in the toolbar.</span></span> <span data-ttu-id="b456f-124">若要這樣做，範例會呼叫 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數來回應 [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) 訊息。</span><span class="sxs-lookup"><span data-stu-id="b456f-124">To do this, the example calls the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function in response to the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span>


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a><span data-ttu-id="b456f-125">處理 Application-Defined 訊息</span><span class="sxs-lookup"><span data-stu-id="b456f-125">Process Application-Defined Messages</span></span>

<span data-ttu-id="b456f-126">當使用者在下拉式方塊中按下 TAB、ENTER 或 ESC 鍵時， **SubClassProc** 函式會將應用程式定義的訊息傳送至工具列視窗。</span><span class="sxs-lookup"><span data-stu-id="b456f-126">The **SubClassProc** function sends application-defined messages to the toolbar window when the user presses the TAB, ENTER, or ESC key in a combo box.</span></span> <span data-ttu-id="b456f-127">傳送的是 [ **wm \_ ]** 索引標籤，以取得 tab 鍵、為 Esc 鍵輸入 **wm \_ ESC** 訊息，以及輸入輸入金鑰的 **wm \_ 輸入** 訊息。</span><span class="sxs-lookup"><span data-stu-id="b456f-127">The **WM\_TAB** message is sent for the TAB key, the **WM\_ESC** message for the ESC key, and the **WM\_ENTER** message for the ENTER key.</span></span>

<span data-ttu-id="b456f-128">此範例會將焦點設為工具列中的下一個下拉式方塊，以處理 WM 索引標籤訊息。 **\_**</span><span class="sxs-lookup"><span data-stu-id="b456f-128">The example processes the **WM\_TAB** message by setting the focus to the next combo box in the toolbar.</span></span> <span data-ttu-id="b456f-129">它會將焦點設定為主應用程式視窗，以處理 **WM \_ ESC** 訊息。</span><span class="sxs-lookup"><span data-stu-id="b456f-129">It processes the **WM\_ESC** message by setting the focus to the main application window.</span></span>


```C++
  case WM_TAB: 
      if (GetFocus() == hwndEdit1) 
          SetFocus(hwndCombo2); 
      else 
          SetFocus(hwndCombo1); 
      break; 
 
  case WM_ESC: 
       hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
       // Clear the current selection. 
       SendMessage(hwndCombo, CB_SETCURSEL, 
          (WPARAM) (-1), 0); 
 
      //  Set the focus to the main window. 
      SetFocus(hwndMain); 
      break;
```



<span data-ttu-id="b456f-130">為了回應 **WM \_ 輸入** 訊息，此範例會確保下拉式方塊的目前選取範圍有效，然後將焦點設定為主要應用程式視窗。</span><span class="sxs-lookup"><span data-stu-id="b456f-130">In response to the **WM\_ENTER** message, the example ensures that the current selection for the combo box is valid and then sets the focus to the main application window.</span></span> <span data-ttu-id="b456f-131">如果下拉式方塊未包含目前的選取範圍，此範例會使用 [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md) 訊息來搜尋符合選取欄位內容的清單專案。</span><span class="sxs-lookup"><span data-stu-id="b456f-131">If the combo box contains no current selection, the example uses the [**CB\_FINDSTRINGEXACT**](cb-findstringexact.md) message to search for a list item that matches the contents of the selection field.</span></span> <span data-ttu-id="b456f-132">如果有相符專案，此範例會設定目前的選取專案;否則，它會新增清單專案。</span><span class="sxs-lookup"><span data-stu-id="b456f-132">If there is a match, the example sets the current selection; otherwise, it adds a new list item.</span></span>


```C++
case WM_ENTER: 
    hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
    SetFocus(hwndMain); 
 
    //  If there is no current selection, set one. 
    if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
            == CB_ERR) 
    { 
        if (SendMessage(hwndCombo, WM_GETTEXT, 
                sizeof(achTemp), (LPARAM) achTemp) == 0) 
            break;      //  Empty selection field 
        dwIndex = SendMessage(hwndCombo, 
            CB_FINDSTRINGEXACT, (WPARAM) (-1), 
            (LPARAM) achTemp); 
 
        //  Add the string, if necessary, and select it. 
        if (dwIndex == CB_ERR) 
            dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                0, (LPARAM) achTemp); 
        if (dwIndex != CB_ERR) 
            SendMessage(hwndCombo, CB_SETCURSEL, 
                dwIndex, 0); 
    } 
    break; 
       
    // . 
    // .  Process additional messages. 
    // . 
 
default: 
    return DefWindowProc(hwnd, msg, wParam, lParam); 
```



## <a name="complete-example"></a><span data-ttu-id="b456f-133">完整範例</span><span class="sxs-lookup"><span data-stu-id="b456f-133">Complete example</span></span>

<span data-ttu-id="b456f-134">以下是兩個下拉式方塊的工具列和子類別程式的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="b456f-134">Following are the window procedure for the toolbar and the subclass procedure for the two combo boxes.</span></span>


```C++
#define WM_TAB (WM_USER) 
#define WM_ESC (WM_USER + 1) 
#define WM_ENTER (WM_USER + 2) 

//  Global variables
HWND    hwndMain; 
WNDPROC lpfnEditWndProc; //  Original wndproc for the combo box 

//  Prototypes
LRESULT CALLBACK SubClassProc( HWND, UINT, WPARAM, LPARAM );
 
/******************************************************** 
 
    FUNCTION:   ToolbarWindowProc 
 
    PURPOSE:    Window procedure for the toolbar window 
 
*********************************************************/ 
 
LRESULT CALLBACK ToolbarWindowProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    static HWND   hwndEdit1; 
    static HWND   hwndEdit2; 
    static HWND   hwndCombo1; 
    static HWND   hwndCombo2; 
    POINT       pt; 
    DWORD       dwBaseUnits; 
    HWND        hwndCombo; 
    DWORD       dwIndex; 
    char achTemp[256];       //  Temporary buffer 
 
    switch (msg) 
    { 
        case WM_CREATE: 
            //  Create two combo box child windows. 
            dwBaseUnits = GetDialogBaseUnits(); 
 
            hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (6 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, NULL, NULL);  
 
            hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (112 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, hInst, NULL); 
            
            //  Get the edit window handle to each combo box. 
            pt.x = 1; 
            pt.y = 1; 
            hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
            hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
            //  Change the window procedure for both edit windows 
            //  to the subclass procedure. 
            lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
                GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
            SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 

            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndCombo1); 
            break; 

        case WM_TAB: 
            if (GetFocus() == hwndEdit1) 
                SetFocus(hwndCombo2); 
            else 
                SetFocus(hwndCombo1); 
            break; 
 
        case WM_ESC: 
             hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
             // Clear the current selection. 
             SendMessage(hwndCombo, CB_SETCURSEL, 
                (WPARAM) (-1), 0); 
 
            //  Set the focus to the main window. 
            SetFocus(hwndMain); 
            break;

        case WM_ENTER: 
            hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
            SetFocus(hwndMain); 
 
            //  If there is no current selection, set one. 
            if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
                    == CB_ERR) 
            { 
                if (SendMessage(hwndCombo, WM_GETTEXT, 
                        sizeof(achTemp), (LPARAM) achTemp) == 0) 
                    break;      //  Empty selection field 
                dwIndex = SendMessage(hwndCombo, 
                    CB_FINDSTRINGEXACT, (WPARAM) (-1), 
                    (LPARAM) achTemp); 
 
                //  Add the string, if necessary, and select it. 
                if (dwIndex == CB_ERR) 
                    dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                        0, (LPARAM) achTemp); 
                if (dwIndex != CB_ERR) 
                    SendMessage(hwndCombo, CB_SETCURSEL, 
                        dwIndex, 0); 
            } 
            break; 
       
            // . 
            // .  Process additional messages. 
            // . 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
/******************************************************** 
 
    FUNCTION:   SubClassProc 
 
    PURPOSE:    Process TAB and ESCAPE keys, and pass all 
                other messages to the class window 
                procedure. 
 
*********************************************************/ 
LRESULT CALLBACK SubClassProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (msg) 
    { 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_TAB: 
                    SendMessage(hwndMain, WM_TAB, 0, 0); 
                    return 0; 
                case VK_ESCAPE: 
                    SendMessage(hwndMain, WM_ESC, 0, 0); 
                    return 0; 
                case VK_RETURN: 
                    SendMessage(hwndMain, WM_ENTER, 0, 0); 
                    return 0; 
            } 
            break; 
 
        case WM_KEYUP: 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case VK_TAB: 
                case VK_ESCAPE: 
                case VK_RETURN: 
                    return 0; 
            } 
    } 
 
    //  Call the original window procedure for default processing. 
     return CallWindowProc(lpfnEditWndProc, hwnd, msg, wParam, lParam); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="b456f-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="b456f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b456f-136">關於下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="b456f-136">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="b456f-137">ComboBox 控制項參考</span><span class="sxs-lookup"><span data-stu-id="b456f-137">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="b456f-138">使用下拉式方塊</span><span class="sxs-lookup"><span data-stu-id="b456f-138">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="b456f-139">ComboBox</span><span class="sxs-lookup"><span data-stu-id="b456f-139">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 