---
title: 如何建立索引標籤式對話方塊
description: 本節中的範例將示範如何建立使用 tab 鍵來提供多個控制項頁面的對話方塊。
ms.assetid: DBF7FBDF-AADC-45CE-833E-F893C1129FC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0b84a8a77d18903ddbdb29687cc2b97b88872b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842788"
---
# <a name="how-to-create-a-tabbed-dialog-box"></a><span data-ttu-id="f83e4-103">如何建立索引標籤式對話方塊</span><span class="sxs-lookup"><span data-stu-id="f83e4-103">How to Create a Tabbed Dialog Box</span></span>

<span data-ttu-id="f83e4-104">本節中的範例將示範如何建立使用 tab 鍵來提供多個控制項頁面的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f83e4-104">The example in this section demonstrates how to create a dialog box that uses tabs to provide multiple pages of controls.</span></span> <span data-ttu-id="f83e4-105">主要對話方塊是強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f83e4-105">The main dialog box is a modal dialog box.</span></span> <span data-ttu-id="f83e4-106">每一頁的控制項都是由具有 [**WS \_ 子**](/windows/desktop/winmsg/window-styles) 樣式的對話方塊範本所定義。</span><span class="sxs-lookup"><span data-stu-id="f83e4-106">Each page of controls is defined by a dialog box template that has the [**WS\_CHILD**](/windows/desktop/winmsg/window-styles) style.</span></span> <span data-ttu-id="f83e4-107">選取索引標籤時，就會為傳入頁面建立非強制回應對話方塊，並終結傳出頁面的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f83e4-107">When a tab is selected, a modeless dialog box is created for the incoming page and the dialog box for the outgoing page is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="f83e4-108">在許多情況下，您可以使用屬性工作表更輕鬆地執行多頁對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f83e4-108">In many cases, you can implement multiple-page dialog boxes more easily by using property sheets.</span></span> <span data-ttu-id="f83e4-109">如需屬性工作表的詳細資訊，請參閱 [關於屬性工作表](property-sheets.md)。</span><span class="sxs-lookup"><span data-stu-id="f83e4-109">For more information about property sheets, see [About Property Sheets](property-sheets.md).</span></span>

 

<span data-ttu-id="f83e4-110">主要對話方塊的範本只會定義兩個按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="f83e4-110">The template for the main dialog box simply defines two button controls.</span></span> <span data-ttu-id="f83e4-111">處理 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息時，對話方塊程式會建立一個索引標籤控制項，並為每個子對話方塊載入對話方塊範本資源。</span><span class="sxs-lookup"><span data-stu-id="f83e4-111">When processing the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message, the dialog box procedure creates a tab control and loads the dialog box template resources for each of the child dialog boxes.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f83e4-112">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="f83e4-112">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f83e4-113">技術</span><span class="sxs-lookup"><span data-stu-id="f83e4-113">Technologies</span></span>

-   [<span data-ttu-id="f83e4-114">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="f83e4-114">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f83e4-115">必要條件</span><span class="sxs-lookup"><span data-stu-id="f83e4-115">Prerequisites</span></span>

-   <span data-ttu-id="f83e4-116">C/C++</span><span class="sxs-lookup"><span data-stu-id="f83e4-116">C/C++</span></span>
-   <span data-ttu-id="f83e4-117">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="f83e4-117">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f83e4-118">指示</span><span class="sxs-lookup"><span data-stu-id="f83e4-118">Instructions</span></span>

### <a name="create-a-tabbed-dialog-box"></a><span data-ttu-id="f83e4-119">建立索引標籤式對話方塊</span><span class="sxs-lookup"><span data-stu-id="f83e4-119">Create a Tabbed Dialog Box</span></span>

<span data-ttu-id="f83e4-120">這項資訊會儲存在名為 DLGHDR 的應用程式定義結構中。</span><span class="sxs-lookup"><span data-stu-id="f83e4-120">The information is saved in an application-defined structure called DLGHDR.</span></span> <span data-ttu-id="f83e4-121">此結構的指標會使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數與對話方塊視窗相關聯。</span><span class="sxs-lookup"><span data-stu-id="f83e4-121">A pointer to this structure is associated with the dialog box window by using the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function.</span></span> <span data-ttu-id="f83e4-122">結構會在應用程式的標頭檔中定義，如下所示。</span><span class="sxs-lookup"><span data-stu-id="f83e4-122">The structure is defined in the application's header file, as follows.</span></span>


```C++
#define C_PAGES 3 

typedef struct tag_dlghdr { 
    HWND hwndTab;       // tab control 
    HWND hwndDisplay;   // current child dialog box 
    RECT rcDisplay;     // display rectangle for the tab control 
    DLGTEMPLATEEX *apRes[C_PAGES]; 
} DLGHDR; 
```



<span data-ttu-id="f83e4-123">下列函式會處理主要對話方塊的 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。</span><span class="sxs-lookup"><span data-stu-id="f83e4-123">The following function processes the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message for the main dialog box.</span></span> <span data-ttu-id="f83e4-124">函式會配置 `DLGHDR` 結構、載入子對話方塊的對話方塊範本資源，以及建立索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="f83e4-124">The function allocates the `DLGHDR` structure, loads the dialog box template resources for the child dialog boxes, and creates the tab control.</span></span>

<span data-ttu-id="f83e4-125">每個子對話方塊的大小是由 [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) 結構所指定。</span><span class="sxs-lookup"><span data-stu-id="f83e4-125">The size of each child dialog box is specified by the [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) structure.</span></span> <span data-ttu-id="f83e4-126">此函式會檢查每個對話方塊的大小，並使用 [**TCM \_ ADJUSTRECT**](tcm-adjustrect.md) 訊息的宏來計算索引標籤控制項的適當大小。</span><span class="sxs-lookup"><span data-stu-id="f83e4-126">The function examines the size of each dialog box and uses the macro for the [**TCM\_ADJUSTRECT**](tcm-adjustrect.md) message to calculate an appropriate size for the tab control.</span></span> <span data-ttu-id="f83e4-127">然後，它會調整對話方塊的大小，並據此放置兩個按鈕。</span><span class="sxs-lookup"><span data-stu-id="f83e4-127">Then it sizes the dialog box and positions the two buttons accordingly.</span></span> <span data-ttu-id="f83e4-128">此範例會使用 [**TabCtrl \_ ADJUSTRECT**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect)宏來傳送 **TCM \_ ADJUSTRECT** 。</span><span class="sxs-lookup"><span data-stu-id="f83e4-128">This example sends **TCM\_ADJUSTRECT** by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>


```C++
// Handles the WM_INITDIALOG message for a dialog box that contains 
//   a tab control used to select among three child dialog boxes.
// Returns a result code.
// hwndDlg - handle of the dialog box.
// 
HRESULT OnTabbedDialogInit(HWND hwndDlg) 
{ 
    INITCOMMONCONTROLSEX iccex;
    DWORD dwDlgBase = GetDialogBaseUnits();
    int cxMargin = LOWORD(dwDlgBase) / 4; 
    int cyMargin = HIWORD(dwDlgBase) / 8; 

    TCITEM tie; 
    RECT rcTab; 
    HWND hwndButton; 
    RECT rcButton; 
    int i; 

    // Initialize common controls.
    iccex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    iccex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&iccex); 

    // Allocate memory for the DLGHDR structure. Remember to 
    // free this memory before the dialog box is destroyed.
    DLGHDR *pHdr = (DLGHDR *) LocalAlloc(LPTR, sizeof(DLGHDR)); 

    // Save a pointer to the DLGHDR structure in the window
    // data of the dialog box. 
    SetWindowLongPtr(hwndDlg, GWLP_USERDATA, (LONG_PTR) pHdr); 
 
    // Create the tab control. Note that g_hInst is a global 
    // instance handle. 
    pHdr->hwndTab = CreateWindow( 
        WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, 100, 100, 
        hwndDlg, NULL, g_hInst, NULL 
        ); 
    if (pHdr->hwndTab == NULL) 
    {
        return HRESULT_FROM_WIN32(GetLastError());
    }
 
    // Add a tab for each of the three child dialog boxes. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = L"First"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 0, &tie); 
    tie.pszText = L"Second"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 1, &tie); 
    tie.pszText = L"Third"; 
    TabCtrl_InsertItem(pHdr->hwndTab, 2, &tie); 

    // Lock the resources for the three child dialog boxes. 
    pHdr->apRes[0] = DoLockDlgRes(MAKEINTRESOURCE(IDD_FIRSTDLG)); 
    pHdr->apRes[1] = DoLockDlgRes(MAKEINTRESOURCE(IDD_SECONDDLG)); 
    pHdr->apRes[2] = DoLockDlgRes(MAKEINTRESOURCE(IDD_THIRDDLG)); 

    // Determine a bounding rectangle that is large enough to 
    // contain the largest child dialog box. 
    SetRectEmpty(&rcTab); 
    for (i = 0; i < C_PAGES; i++) 
    { 
        if (pHdr->apRes[i]->cx > rcTab.right) 
            rcTab.right = pHdr->apRes[i]->cx; 
        if (pHdr->apRes[i]->cy > rcTab.bottom) 
            rcTab.bottom = pHdr->apRes[i]->cy; 
    }

    // Map the rectangle from dialog box units to pixels.
    MapDialogRect(hwndDlg, &rcTab);
    
    // Calculate how large to make the tab control, so 
    // the display area can accommodate all the child dialog boxes. 
    TabCtrl_AdjustRect(pHdr->hwndTab, TRUE, &rcTab); 
    OffsetRect(&rcTab, cxMargin - rcTab.left, cyMargin - rcTab.top); 
 
    // Calculate the display rectangle. 
    CopyRect(&pHdr->rcDisplay, &rcTab); 
    TabCtrl_AdjustRect(pHdr->hwndTab, FALSE, &pHdr->rcDisplay); 
 
    // Set the size and position of the tab control, buttons, 
    // and dialog box. 
    SetWindowPos(pHdr->hwndTab, NULL, rcTab.left, rcTab.top, 
            rcTab.right - rcTab.left, rcTab.bottom - rcTab.top, 
            SWP_NOZORDER); 
 
    // Move the first button below the tab control. 
    hwndButton = GetDlgItem(hwndDlg, IDB_CLOSE); 
    SetWindowPos(hwndButton, NULL, 
            rcTab.left, rcTab.bottom + cyMargin, 0, 0, 
            SWP_NOSIZE | SWP_NOZORDER); 
 
    // Determine the size of the button. 
    GetWindowRect(hwndButton, &rcButton); 
    rcButton.right -= rcButton.left; 
    rcButton.bottom -= rcButton.top; 
 
    // Move the second button to the right of the first. 
    hwndButton = GetDlgItem(hwndDlg, IDB_TEST); 
    SetWindowPos(hwndButton, NULL, 
        rcTab.left + rcButton.right + cxMargin, 
        rcTab.bottom + cyMargin, 0, 0, 
        SWP_NOSIZE | SWP_NOZORDER); 
 
    // Size the dialog box. 
    SetWindowPos(hwndDlg, NULL, 0, 0, 
        rcTab.right + cyMargin + (2 * GetSystemMetrics(SM_CXDLGFRAME)), 
        rcTab.bottom + rcButton.bottom + (2 * cyMargin)
        + (2 * GetSystemMetrics(SM_CYDLGFRAME)) 
        + GetSystemMetrics(SM_CYCAPTION), 
        SWP_NOMOVE | SWP_NOZORDER); 
 
    // Simulate selection of the first item. 
    OnSelChanged(hwndDlg); 

    return S_OK;
} 

// Loads and locks a dialog box template resource. 
// Returns the address of the locked dialog box template resource. 
// lpszResName - name of the resource. 
//
DLGTEMPLATEEX* DoLockDlgRes(LPCTSTR lpszResName) 
{ 
    HRSRC hrsrc = FindResource(NULL, lpszResName, RT_DIALOG); 

    // Note that g_hInst is the global instance handle
    HGLOBAL hglb = LoadResource(g_hInst, hrsrc);  
    return (DLGTEMPLATEEX *) LockResource(hglb); 
} 
```



<span data-ttu-id="f83e4-129">下列函式會處理主要對話方塊的 [TCN \_ SELCHANGE](tcn-selchange.md) 通知程式碼。</span><span class="sxs-lookup"><span data-stu-id="f83e4-129">The following function processes the [TCN\_SELCHANGE](tcn-selchange.md) notification code for the main dialog box.</span></span> <span data-ttu-id="f83e4-130">函數會終結外寄頁面的對話方塊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="f83e4-130">The function destroys the dialog box for the outgoing page, if any.</span></span> <span data-ttu-id="f83e4-131">然後，它會使用 [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) 函式來建立傳入頁面的非強制回應對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f83e4-131">Then it uses the [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) function to create a modeless dialog box for the incoming page.</span></span>


```C++
// Processes the TCN_SELCHANGE notification. 
// hwndDlg - handle to the parent dialog box. 
//
VOID OnSelChanged(HWND hwndDlg) 
{ 
    // Get the dialog header data.
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndDlg, GWLP_USERDATA); 

    // Get the index of the selected tab.
    int iSel = TabCtrl_GetCurSel(pHdr->hwndTab); 
 
    // Destroy the current child dialog box, if any. 
    if (pHdr->hwndDisplay != NULL) 
        DestroyWindow(pHdr->hwndDisplay); 
 
    // Create the new child dialog box. Note that g_hInst is the
    // global instance handle.
    pHdr->hwndDisplay = CreateDialogIndirect(g_hInst, 
        (DLGTEMPLATE *)pHdr->apRes[iSel], hwndDlg, ChildDialogProc); 

    return;
} 
```



<span data-ttu-id="f83e4-132">下列函式會為每個子對話方塊處理 [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) 訊息。</span><span class="sxs-lookup"><span data-stu-id="f83e4-132">The following function processes the [**WM\_INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) message for each of the child dialog boxes.</span></span> <span data-ttu-id="f83e4-133">您無法指定使用 [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) 函數建立之對話方塊的位置。</span><span class="sxs-lookup"><span data-stu-id="f83e4-133">You cannot specify the position of a dialog box that is created using the [**CreateDialogIndirect**](/windows/desktop/api/winuser/nf-winuser-createdialogindirecta) function.</span></span> <span data-ttu-id="f83e4-134">此函式會使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函式，在索引標籤控制項的顯示區域內放置子對話。</span><span class="sxs-lookup"><span data-stu-id="f83e4-134">This function uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to position the child dialog within the tab control's display area.</span></span>


```C++
// Positions the child dialog box to occupy the display area of the 
//   tab control. 
// hwndDlg - handle of the dialog box.
//
VOID WINAPI OnChildDialogInit(HWND hwndDlg) 
{ 
    HWND hwndParent = GetParent(hwndDlg);
    DLGHDR *pHdr = (DLGHDR *) GetWindowLongPtr( 
        hwndParent, GWLP_USERDATA); 
    SetWindowPos(hwndDlg, NULL, pHdr->rcDisplay.left,
        pHdr->rcDisplay.top,//-2,
        (pHdr->rcDisplay.right - pHdr->rcDisplay.left),
        (pHdr->rcDisplay.bottom - pHdr->rcDisplay.top),
        SWP_SHOWWINDOW);
        
    return;
}
```



## <a name="related-topics"></a><span data-ttu-id="f83e4-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f83e4-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f83e4-136">使用索引標籤控制項</span><span class="sxs-lookup"><span data-stu-id="f83e4-136">Using Tab Controls</span></span>](using-tab-controls.md)
</dt> <dt>

<span data-ttu-id="f83e4-137">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="f83e4-137">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 