---
title: 如何在主視窗中建立索引標籤控制項
description: 本節中的範例將示範如何建立索引標籤控制項，並將其顯示在應用程式主視窗的工作區中。
ms.assetid: 24157B8B-177B-471C-9DA0-548D09EA5F89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 686a9a4fe4f6be95ccdcf3bbcb597c2c48ff3b2d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463769"
---
# <a name="how-to-create-a-tab-control-in-the-main-window"></a><span data-ttu-id="7a0fb-103">如何在主視窗中建立索引標籤控制項</span><span class="sxs-lookup"><span data-stu-id="7a0fb-103">How to Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="7a0fb-104">本節中的範例將示範如何建立索引標籤控制項，並將其顯示在應用程式主視窗的工作區中。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-104">The example in this section demonstrates how to create a tab control and display it in the client area of the application's main window.</span></span> <span data-ttu-id="7a0fb-105">應用程式會在索引標籤控制項的顯示區域中，顯示 (靜態控制項) 的第三個視窗。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-105">The application displays a third window (a static control) in the display area of the tab control.</span></span> <span data-ttu-id="7a0fb-106">父視窗在處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息時，會定位並調整索引標籤控制項和靜態控制項的大小。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-106">The parent window positions and sizes the tab control and static control when it processes the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message.</span></span>

<span data-ttu-id="7a0fb-107">此範例中有七個索引標籤，一周的每一天都有一個。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-107">There are seven tabs in this example, one for each day of the week.</span></span> <span data-ttu-id="7a0fb-108">當使用者選取索引標籤時，應用程式會在靜態控制項中顯示對應日期的名稱。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-108">When the user selects a tab, the application displays the name of the corresponding day in the static control.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7a0fb-109">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="7a0fb-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7a0fb-110">技術</span><span class="sxs-lookup"><span data-stu-id="7a0fb-110">Technologies</span></span>

-   [<span data-ttu-id="7a0fb-111">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="7a0fb-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7a0fb-112">必要條件</span><span class="sxs-lookup"><span data-stu-id="7a0fb-112">Prerequisites</span></span>

-   <span data-ttu-id="7a0fb-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="7a0fb-113">C/C++</span></span>
-   <span data-ttu-id="7a0fb-114">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="7a0fb-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7a0fb-115">指示</span><span class="sxs-lookup"><span data-stu-id="7a0fb-115">Instructions</span></span>

### <a name="create-a-tab-control-in-the-main-window"></a><span data-ttu-id="7a0fb-116">在主視窗中建立索引標籤控制項</span><span class="sxs-lookup"><span data-stu-id="7a0fb-116">Create a Tab Control in the Main Window</span></span>

<span data-ttu-id="7a0fb-117">下列函式會建立索引標籤控制項，並為每一周的每一天加入索引標籤。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-117">The following function creates the tab control and adds a tab for each day of the week.</span></span> <span data-ttu-id="7a0fb-118">天數的名稱會定義為字串資源，並以識別碼星期日為開頭的連續編號 \_ (在應用程式的資源標頭檔) 中定義。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-118">The names of the days are defined as string resources, consecutively numbered starting with IDS\_SUNDAY (defined in the application's resource header file).</span></span> <span data-ttu-id="7a0fb-119">父視窗和索引標籤控制項都必須有 [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) 視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-119">Both the parent window and the tab control must have the [**WS\_CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles) window style.</span></span> <span data-ttu-id="7a0fb-120">在建立主視窗之後，應用程式的初始化函式會呼叫這個函式。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-120">The application's initialization function calls this function after creating the main window.</span></span>


```C++
#define DAYS_IN_WEEK 7

// Creates a tab control, sized to fit the specified parent window's client
//   area, and adds some tabs. 
// Returns the handle to the tab control. 
// hwndParent - parent window (the application's main window). 
// 
HWND DoCreateTabControl(HWND hwndParent) 
{ 
    RECT rcClient; 
    INITCOMMONCONTROLSEX icex;
    HWND hwndTab; 
    TCITEM tie; 
    int i; 
    TCHAR achTemp[256];  // Temporary buffer for strings.
 
    // Initialize common controls.
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_TAB_CLASSES;
    InitCommonControlsEx(&icex);
    
    // Get the dimensions of the parent window's client area, and 
    // create a tab control child window of that size. Note that g_hInst
    // is the global instance handle.
    GetClientRect(hwndParent, &rcClient); 
    hwndTab = CreateWindow(WC_TABCONTROL, L"", 
        WS_CHILD | WS_CLIPSIBLINGS | WS_VISIBLE, 
        0, 0, rcClient.right, rcClient.bottom, 
        hwndParent, NULL, g_hInst, NULL); 
    if (hwndTab == NULL)
    { 
        return NULL; 
    }
 
    // Add tabs for each day of the week. 
    tie.mask = TCIF_TEXT | TCIF_IMAGE; 
    tie.iImage = -1; 
    tie.pszText = achTemp; 
 
    for (i = 0; i < DAYS_IN_WEEK; i++) 
    { 
        // Load the day string from the string resources. Note that
        // g_hInst is the global instance handle.
        LoadString(g_hInst, IDS_SUNDAY + i, 
                achTemp, sizeof(achTemp) / sizeof(achTemp[0])); 
        if (TabCtrl_InsertItem(hwndTab, i, &tie) == -1) 
        { 
            DestroyWindow(hwndTab); 
            return NULL; 
        } 
    } 
    return hwndTab; 
} 
```



<span data-ttu-id="7a0fb-121">下列函式會建立位於索引標籤控制項之顯示區域中的靜態控制項。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-121">The following function creates the static control that resides in the tab control's display area.</span></span> <span data-ttu-id="7a0fb-122">應用程式的初始化函式會在建立主視窗和索引標籤控制項之後，呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-122">The application's initialization function calls this function after creating the main window and the tab control.</span></span>


```C++
// Creates a child window (a static control) to occupy the tab control's 
//   display area. 
// Returns the handle to the static control. 
// hwndTab - handle of the tab control. 
// 
HWND DoCreateDisplayWindow(HWND hwndTab) 
{ 
    HWND hwndStatic = CreateWindow(WC_STATIC, L"", 
        WS_CHILD | WS_VISIBLE | WS_BORDER, 
        100, 100, 100, 100,        // Position and dimensions; example only.
        hwndTab, NULL, g_hInst,    // g_hInst is the global instance handle
        NULL); 
    return hwndStatic; 
}
```



<span data-ttu-id="7a0fb-123">下列範例函數是從應用程式的視窗程式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-123">The following example functions are called from the application's window procedure.</span></span> <span data-ttu-id="7a0fb-124">應用程式會 `OnSize` 在處理 [**WM \_ 大小**](/windows/desktop/winmsg/wm-size) 訊息時呼叫函式，以定位並調整索引標籤控制項的大小，以符合主視窗的工作區。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-124">The application calls the `OnSize` function when processing the [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) message to position and size the tab control to fit the main window's client area.</span></span>

<span data-ttu-id="7a0fb-125">選取索引標籤時，索引標籤控制項會傳送 [**WM \_ 通知**](wm-notify.md) 訊息，指定 [TCN \_ SELCHANGE](tcn-selchange.md) 通知碼。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-125">When a tab is selected, the tab control sends a [**WM\_NOTIFY**](wm-notify.md) message, specifying the [TCN\_SELCHANGE](tcn-selchange.md) notification code.</span></span> <span data-ttu-id="7a0fb-126">應用程式的函式會藉 `OnNotify` 由設定靜態控制項的文字來處理此通知碼。</span><span class="sxs-lookup"><span data-stu-id="7a0fb-126">The application's `OnNotify` function processes this notification code by setting the text of the static control.</span></span>


```C++
// Handles the WM_SIZE message for the main window by resizing the 
//   tab control. 
// hwndTab - handle of the tab control.
// lParam - the lParam parameter of the WM_SIZE message.
//
HRESULT OnSize(HWND hwndTab, LPARAM lParam)
{
    RECT rc; 

    if (hwndTab == NULL)
        return E_INVALIDARG;

    // Resize the tab control to fit the client are of main window.
     if (!SetWindowPos(hwndTab, HWND_TOP, 0, 0, GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), SWP_SHOWWINDOW))
        return E_FAIL;

    return S_OK;
}

// Handles notifications from the tab control, as follows: 
//   TCN_SELCHANGING - always returns FALSE to allow the user to select a 
//     different tab.  
//   TCN_SELCHANGE - loads a string resource and displays it in a static 
//     control on the selected tab.
// hwndTab - handle of the tab control.
// hwndDisplay - handle of the static control. 
// lParam - the lParam parameter of the WM_NOTIFY message.
//
BOOL OnNotify(HWND hwndTab, HWND hwndDisplay, LPARAM lParam)
{
    TCHAR achTemp[256]; // temporary buffer for strings

    switch (((LPNMHDR)lParam)->code)
        {
            case TCN_SELCHANGING:
                {
                    // Return FALSE to allow the selection to change.
                    return FALSE;
                }

            case TCN_SELCHANGE:
                { 
                    int iPage = TabCtrl_GetCurSel(hwndTab); 

                    // Note that g_hInst is the global instance handle.
                    LoadString(g_hInst, IDS_SUNDAY + iPage, achTemp,
                        sizeof(achTemp) / sizeof(achTemp[0])); 
                    LRESULT result = SendMessage(hwndDisplay, WM_SETTEXT, 0,
                        (LPARAM) achTemp); 
                    break;
                } 
        }
        return TRUE;
}
```



## <a name="related-topics"></a><span data-ttu-id="7a0fb-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="7a0fb-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a0fb-128">使用索引標籤控制項</span><span class="sxs-lookup"><span data-stu-id="7a0fb-128">Using Tab Controls</span></span>](using-tab-controls.md)
</dt> <dt>

<span data-ttu-id="7a0fb-129">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="7a0fb-129">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 