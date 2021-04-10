---
title: 如何建立 Up-Down 控制項
description: 您可以藉由呼叫 CreateWindowEx 函式，並傳遞 \_ Windows 類別參數 lpClassName 的值上下按鈕類別，來建立新的控制項。
ms.assetid: 9B7A5F8B-4EE5-413B-A60C-800758DD1120
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427361d7748270ad9c689867aa8100e95afbd6b0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093415"
---
# <a name="how-to-create-up-down-controls"></a><span data-ttu-id="cbaf4-103">如何建立 Up-Down 控制項</span><span class="sxs-lookup"><span data-stu-id="cbaf4-103">How to Create Up-Down Controls</span></span>

<span data-ttu-id="cbaf4-104">您可以藉由呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)函式，並傳遞 Windows 類別參數 *LpClassName* 的值 [**上下按鈕 \_ 類別**](common-control-window-classes.md)，來建立新的控制項。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-104">You create up-down controls by calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and passing the value [**UPDOWN\_CLASS**](common-control-window-classes.md) for the Windows class parameter *lpClassName*.</span></span>

<span data-ttu-id="cbaf4-105">**注意**   [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol)函式已被取代。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-105">**Note**   The [**CreateUpDownControl**](/windows/desktop/api/Commctrl/nf-commctrl-createupdowncontrol) function is deprecated.</span></span> <span data-ttu-id="cbaf4-106">您應該改為使用 `CreateWindowEx` 函數。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-106">You should use the `CreateWindowEx` function instead.</span></span>

<span data-ttu-id="cbaf4-107">本主題中所述的程式碼範例會使用上下按鈕控制項來驅動進度列。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-107">The code example featured in this topic uses an up-down control to drive a progress bar.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="cbaf4-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="cbaf4-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="cbaf4-109">技術</span><span class="sxs-lookup"><span data-stu-id="cbaf4-109">Technologies</span></span>

-   [<span data-ttu-id="cbaf4-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="cbaf4-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="cbaf4-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="cbaf4-111">Prerequisites</span></span>

-   <span data-ttu-id="cbaf4-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="cbaf4-112">C/C++</span></span>
-   <span data-ttu-id="cbaf4-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="cbaf4-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="cbaf4-114">指示</span><span class="sxs-lookup"><span data-stu-id="cbaf4-114">Instructions</span></span>

### <a name="step-1-add-references-to-the-common-controls"></a><span data-ttu-id="cbaf4-115">步驟1：將參考加入至通用控制項</span><span class="sxs-lookup"><span data-stu-id="cbaf4-115">Step 1: Add References to the Common Controls</span></span>

<span data-ttu-id="cbaf4-116">除了新增預處理器指示詞以包含通用控制項標頭檔之外，您還必須設定連結器參考最新版本的通用控制項程式庫。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-116">Besides adding a preprocessor directive to include the common controls header file, you must also configure the linker to reference the latest version of the common controls library.</span></span>


```C++
#include <commctrl.h>

#pragma comment(lib, "C:\\Program Files\\Microsoft SDKs\\Windows\\v7.1\\Lib\\ComCtl32.Lib")

#pragma comment(linker,"\"/manifestdependency:type                  = 'win32' \
                                              name                  = 'Microsoft.Windows.Common-Controls' \
                                              version               = '6.0.0.0' \
                                              processorArchitecture = '*' \
                                              publicKeyToken        = '6595b64144ccf1df' \
                                              language              = '*'\"")
```



### <a name="step-2-forward-declarations"></a><span data-ttu-id="cbaf4-117">步驟2：轉寄宣告</span><span class="sxs-lookup"><span data-stu-id="cbaf4-117">Step 2: Forward Declarations</span></span>

<span data-ttu-id="cbaf4-118">宣告向下控制項和其同級控制項的控制碼，並向前參考初始化和建立控制項的函式。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-118">Declare handles to the up-down control and to its sibling controls, and forward reference the functions that initialize and create the controls.</span></span>


```C++
INITCOMMONCONTROLSEX icex;    // Structure for control initialization.

const UINT valMin=0;          // The range of values for the Up-Down control.
const UINT valMax=100;

RECT rcClient;               // Client area of parent window (Dialog Box).
UINT cyVScroll;              // Height of scroll bar arrow.

HWND hControl       = NULL;  // Handles to the controls.
HWND hwndGroupBox   = NULL;
HWND hwndLabel      = NULL;
HWND hwndUpDnEdtBdy = NULL;
HWND hwndUpDnCtl    = NULL;
HWND hwndProgBar    = NULL;

HWND CreateGroupBox(HWND);   // Handles to the create controls functions.
HWND CreateLabel(HWND);
HWND CreateUpDnBuddy(HWND);
HWND CreateUpDnCtl(HWND);
HWND CreateProgBar(HWND);
```



<span data-ttu-id="cbaf4-119">針對下一個控制項的父對話方塊，宣告視窗處理器的向前參考。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-119">Declare a forward reference to the window processor for the up-down control's parent dialog.</span></span>


```C++
INT_PTR CALLBACK UpDownDialogProc(HWND, UINT, WPARAM, LPARAM);
```



### <a name="step-3-initialize-the-initcommoncontrolsex-structures-dwsize-member"></a><span data-ttu-id="cbaf4-120">步驟3：初始化 INITCOMMONCONTROLSEX 結構的 **dwSize** 成員</span><span class="sxs-lookup"><span data-stu-id="cbaf4-120">Step 3: Initialize the INITCOMMONCONTROLSEX Structure's **dwSize** Member</span></span>

<span data-ttu-id="cbaf4-121">[**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)結構會攜帶用來從 DLL 載入通用控制項類別的資訊。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-121">The [**INITCOMMONCONTROLSEX**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) structure carries the information used to load common control classes from the DLL.</span></span> <span data-ttu-id="cbaf4-122">此結構會搭配 **InitCommonControlsEx** 函式使用，這需要結構的大小才能完成其工作。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-122">This structure is used with the **InitCommonControlsEx** function, which requires the structure's size in order to do its job.</span></span>


```C++
icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
```



> [!Note]  
> <span data-ttu-id="cbaf4-123">您只需要初始化 **dwSize** 成員一次，但您必須在每次建立通用控制項時呼叫 **InitCommonControlsEx** 函數。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-123">You only need to initialize the **dwSize** member once, but you must call the **InitCommonControlsEx** function each time you create a common control.</span></span>

 

### <a name="step-4-create-a-parent-dialog-box-to-host-the-up-down-control"></a><span data-ttu-id="cbaf4-124">步驟4：建立父對話方塊來裝載 Up-Down 控制項</span><span class="sxs-lookup"><span data-stu-id="cbaf4-124">Step 4: Create a Parent Dialog Box to Host the Up-Down Control</span></span>

<span data-ttu-id="cbaf4-125">您可以在主視窗處理器 (*WndProc*) 的訊息處理常式中執行此程式。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-125">You can implement this as a message handler in the main window processor (*WndProc*).</span></span>


```C++
case WM_COMMAND:

    wmId    = LOWORD(wParam);
    wmEvent = HIWORD(wParam);

    switch (wmId)
    {
        case IDM_RUN_UPDOWN:
            DialogBox(g_hInst, MAKEINTRESOURCE(IDD_UPDOWN), hWnd, UpDownDialogProc);
            break;

        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;

        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    break;
```



### <a name="step-5-implement-a-window-processor-for-the-up-down-controls-parent-window"></a><span data-ttu-id="cbaf4-126">步驟5：針對 Up-Down 控制項的父視窗，執行視窗處理器</span><span class="sxs-lookup"><span data-stu-id="cbaf4-126">Step 5: Implement a Window Processor for the Up-Down Control's Parent Window</span></span>

<span data-ttu-id="cbaf4-127">建立父對話方塊時，它會以其子視窗（其父代的控制項）進行初始化。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-127">When the parent dialog box is created, it is initialized with its child windows—the controls that it parents.</span></span> <span data-ttu-id="cbaf4-128">當使用者按一下其中一個下拉式控制項的箭號時，作業系統會將包含通知碼 **UDN \_ DELTAPOS** 的 **WM \_ 通知** 訊息傳送給它，藉此通知事件的對話，後者又包含了有關好友視窗新值的資訊。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-128">When the user clicks one of the up-down control's arrows, the operating system notifies the dialog of the event by sending it a **WM\_NOTIFY** message that contains the notification code **UDN\_DELTAPOS**, which in turn contains information about the buddy window's new value.</span></span> <span data-ttu-id="cbaf4-129">**WM \_ 通知** 訊息處理常式會使用這種新資訊來更新進度列。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-129">The **WM\_NOTIFY** message handler updates the progress bar with this new information.</span></span>


```C++
INT_PTR CALLBACK UpDownDialogProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    UINT nCode;
    int iPosIndicated;
    LPNMUPDOWN lpnmud;

    switch (message)
    {
        case WM_INITDIALOG:
            GetClientRect(hDlg, &rcClient);
            
            cyVScroll = GetSystemMetrics(SM_CYVSCROLL);

            hwndGroupBox   = CreateGroupBox(hDlg);   // Group the controls.
            hwndLabel      = CreateLabel(hDlg);      // Create a label for the Up-Down control.
            hwndUpDnEdtBdy = CreateUpDnBuddy(hDlg);  // Create an buddy window (an Edit control).
            hwndUpDnCtl    = CreateUpDnCtl(hDlg);    // Create an Up-Down control.
            hwndProgBar    = CreateProgBar(hDlg);    // Create a Progress bar,
                                                     // to reflect the state of the Up-down control.

            return (INT_PTR)TRUE;

        case WM_NOTIFY:
            nCode = ((LPNMHDR)lParam)->code;

            switch (nCode)
            {
                case UDN_DELTAPOS:
                    lpnmud  = (LPNMUPDOWN)lParam;
                    iPosIndicated = SendMessage(hwndProgBar, PBM_GETPOS, (WPARAM)0, (LPARAM)0);

                    SendMessage(hwndProgBar,
                                PBM_SETPOS,
                                (WPARAM)(iPosIndicated + lpnmud->iDelta),  // iPosIndicated can have
                                (LPARAM)0);                                // any signed integer value.

                    break;
            }

        case WM_COMMAND:
            if (LOWORD(wParam) == IDOK || LOWORD(wParam) == IDCANCEL)
            {
                EndDialog(hDlg, LOWORD(wParam));
                return TRUE;
            }
            break;
    }
    return FALSE;
}
```



### <a name="step-6-create-the-buddy-window"></a><span data-ttu-id="cbaf4-130">步驟6：建立好友視窗</span><span class="sxs-lookup"><span data-stu-id="cbaf4-130">Step 6: Create the Buddy Window</span></span>

<span data-ttu-id="cbaf4-131">上下控制項的合作者視窗是編輯控制項，而編輯控制項則屬於標準通用控制項的類別。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-131">The up-down control's buddy window is an edit control, and edit controls belong to the class of standard common controls.</span></span> <span data-ttu-id="cbaf4-132">若要使用編輯控制項，請使用「 **ICC \_ 標準 \_ 類別** 初始化」旗標來呼叫 **InitCommonControlsEx** 函數。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-132">To use an edit control, call the **InitCommonControlsEx** function with the **ICC\_STANDARD\_CLASSES** initialization flag.</span></span>


```C++
HWND CreateUpDnBuddy(HWND hwndParent)
{
    icex.dwICC = ICC_STANDARD_CLASSES;    // Set the Initialization Flag value.
    InitCommonControlsEx(&icex);          // Initialize the Common Controls Library to use 
                                          // Buttons, Edit Controls, Static Controls, Listboxes, 
                                          // Comboboxes, and  Scroll Bars.

    hControl = CreateWindowEx(WS_EX_LEFT | WS_EX_CLIENTEDGE | WS_EX_CONTEXTHELP,    //Extended window styles.
                              WC_EDIT,
                              NULL,
                              WS_CHILDWINDOW | WS_VISIBLE | WS_BORDER    // Window styles.
                              | ES_NUMBER | ES_LEFT,                     // Edit control styles.
                              rcClient.left+160, rcClient.top+40,
                              rcClient.left+52, rcClient.top+23,
                              hwndParent,
                              NULL,
                              g_hInst,
                              NULL);

    return (hControl);
}
```



### <a name="step-7-create-the-up-down-control"></a><span data-ttu-id="cbaf4-133">步驟7：建立 Up-Down 控制項</span><span class="sxs-lookup"><span data-stu-id="cbaf4-133">Step 7: Create the Up-Down Control</span></span>

<span data-ttu-id="cbaf4-134">由上而下的控制項屬於上下類別。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-134">Up-down controls belong to the up-down class.</span></span> <span data-ttu-id="cbaf4-135">若要使用上下按鈕控制項，請使用 **ICC \_ 上下按鈕 \_ 類別** 初始化旗標來呼叫 **InitCommonControlsEx** 函數。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-135">To use an up-down control, call the **InitCommonControlsEx** function with the **ICC\_UPDOWN\_CLASS** initialization flag.</span></span> <span data-ttu-id="cbaf4-136">若要在使用者按一下控制項的向上箭號時，讓控制項向上計數，您必須設定上下按鈕控制項的範圍和方向。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-136">To get the control to count upward when the user clicks the control's up arrow, you must set the up-down control's range and direction.</span></span> <span data-ttu-id="cbaf4-137">若要這麼做，您可以傳送包含上限和下限值的 **UDM \_ SETRANGE** 訊息給控制項。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-137">You do this by sending the control a **UDM\_SETRANGE** message that contains values for upper and lower bounds.</span></span>


```C++
HWND CreateUpDnCtl(HWND hwndParent)
{
    icex.dwICC = ICC_UPDOWN_CLASS;    // Set the Initialization Flag value.
    InitCommonControlsEx(&icex);      // Initialize the Common Controls Library.

    hControl = CreateWindowEx(WS_EX_LEFT | WS_EX_LTRREADING,
                              UPDOWN_CLASS,
                              NULL,
                              WS_CHILDWINDOW | WS_VISIBLE
                              | UDS_AUTOBUDDY | UDS_SETBUDDYINT | UDS_ALIGNRIGHT | UDS_ARROWKEYS | UDS_HOTTRACK,
                              0, 0,
                              0, 0,         // Set to zero to automatically size to fit the buddy window.
                              hwndParent,
                              NULL,
                              g_hInst,
                              NULL);

    SendMessage(hControl, UDM_SETRANGE, 0, MAKELPARAM(valMax, valMin));    // Sets the controls direction 
                                                                           // and range.

    return (hControl);
}
```



## <a name="up-down-control-sample-code"></a><span data-ttu-id="cbaf4-138">Up-Down 控制項範例程式碼</span><span class="sxs-lookup"><span data-stu-id="cbaf4-138">Up-Down Control Sample Code</span></span>

<span data-ttu-id="cbaf4-139">這是完整的上下按鈕程式碼範例執行。</span><span class="sxs-lookup"><span data-stu-id="cbaf4-139">This is the complete implementation of the UpDown code sample.</span></span> <span data-ttu-id="cbaf4-140">您可以藉由建立空白的 Win32 專案、將此程式碼複製並貼到空白的 c + + 檔案中，然後新增您自己的標頭檔、RC 檔案、資源 .h 檔案，以及 (.ico) 的圖示檔來進行實驗。 \*</span><span class="sxs-lookup"><span data-stu-id="cbaf4-140">You can experiment with it by creating a blank Win32 project, copying and pasting this code into an empty C++ file, and then adding your own header file, RC file, resource.h file, and an icon file (\*.ico).</span></span>


```C++
// UpDown.cpp : Defines the entry point for the application.

#include "UpDown.h"


#include <commctrl.h>

#pragma comment(lib, "C:\\Program Files\\Microsoft SDKs\\Windows\\v7.1\\Lib\\ComCtl32.Lib")

#pragma comment(linker,"\"/manifestdependency:type                  = 'win32' \
                                              name                  = 'Microsoft.Windows.Common-Controls' \
                                              version               = '6.0.0.0' \
                                              processorArchitecture = '*' \
                                              publicKeyToken        = '6595b64144ccf1df' \
                                              language              = '*'\"")

#define MAX_LOADSTRING 100

HINSTANCE    g_hInst;                            // Global handle to the current instance.
TCHAR        g_szTitle[MAX_LOADSTRING];          // The title bar text.
TCHAR        g_szWindowClass[MAX_LOADSTRING];    // The main window class name.


INITCOMMONCONTROLSEX icex;    // Structure for control initialization.

const UINT valMin=0;          // The range of values for the Up-Down control.
const UINT valMax=100;

RECT rcClient;               // Client area of parent window (Dialog Box).
UINT cyVScroll;              // Height of scroll bar arrow.

HWND hControl       = NULL;  // Handles to the controls.
HWND hwndGroupBox   = NULL;
HWND hwndLabel      = NULL;
HWND hwndUpDnEdtBdy = NULL;
HWND hwndUpDnCtl    = NULL;
HWND hwndProgBar    = NULL;

HWND CreateGroupBox(HWND);   // Handles to the create controls functions.
HWND CreateLabel(HWND);
HWND CreateUpDnBuddy(HWND);
HWND CreateUpDnCtl(HWND);
HWND CreateProgBar(HWND);

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);


INT_PTR CALLBACK UpDownDialogProc(HWND, UINT, WPARAM, LPARAM);

ATOM MyRegisterClass(HINSTANCE hInstance);
BOOL InitInstance(HINSTANCE, int);

int APIENTRY _tWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPTSTR lpCmdLine, int nCmdShow)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG    msg;
    HACCEL hAccelTable;

    LoadString(hInstance, IDS_APP_TITLE, g_szTitle,       MAX_LOADSTRING);
    LoadString(hInstance, IDC_UPDOWN,    g_szWindowClass, MAX_LOADSTRING);

    MyRegisterClass(hInstance);

    if (!InitInstance (hInstance, nCmdShow))
        return FALSE;

    hAccelTable = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDC_UPDOWN));

    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    return (int) msg.wParam;
}
ATOM MyRegisterClass(HINSTANCE hInstance)
{
    WNDCLASSEX wcex;

    wcex.cbSize        = sizeof(WNDCLASSEX);
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = 0;
    wcex.hInstance     = hInstance;
    wcex.hIcon         = LoadIcon(hInstance, MAKEINTRESOURCE(IDI_UpDown));
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);
    wcex.lpszMenuName  = MAKEINTRESOURCE(IDM_MAIN);
    wcex.lpszClassName = g_szWindowClass;
    wcex.hIconSm       = LoadIcon(wcex.hInstance, MAKEINTRESOURCE(IDI_UpDown));

    return RegisterClassEx(&wcex);
}
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
    HWND hWnd;
    g_hInst = hInstance;    // Store instance handle in our global variable.

    hWnd = CreateWindow(g_szWindowClass,                // Class.
                        g_szTitle,                      // Window title.
                        WS_OVERLAPPEDWINDOW,            // Window style.
                        CW_USEDEFAULT, 0,               // Coordinates of top left corner.
                        CW_USEDEFAULT, 0,               // Width and height.
                        NULL, NULL, hInstance, NULL);
    if (!hWnd)
        return FALSE;

    ShowWindow(hWnd, nCmdShow);
    UpdateWindow(hWnd);

    return TRUE;
}
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    UINT wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);

    switch (message)
    {
        case WM_CREATE:
            return TRUE;
            break;

        case WM_COMMAND:

            wmId    = LOWORD(wParam);
            wmEvent = HIWORD(wParam);

            switch (wmId)
            {
                case IDM_RUN_UPDOWN:
                    DialogBox(g_hInst, MAKEINTRESOURCE(IDD_UPDOWN), hWnd, UpDownDialogProc);
                    break;

                case IDM_EXIT:
                    DestroyWindow(hWnd);
                    break;

                default:
                    return DefWindowProc(hWnd, message, wParam, lParam);
            }
            break;
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);

            EndPaint(hWnd, &ps);
            break;

        case WM_DESTROY:
            PostQuitMessage(0);
            break;

        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}

INT_PTR CALLBACK UpDownDialogProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    UINT nCode;
    int iPosIndicated;
    LPNMUPDOWN lpnmud;

    switch (message)
    {
        case WM_INITDIALOG:
            GetClientRect(hDlg, &rcClient);
            
            cyVScroll = GetSystemMetrics(SM_CYVSCROLL);

            hwndGroupBox   = CreateGroupBox(hDlg);   // Group the controls.
            hwndLabel      = CreateLabel(hDlg);      // Create a label for the Up-Down control.
            hwndUpDnEdtBdy = CreateUpDnBuddy(hDlg);  // Create an buddy window (an Edit control).
            hwndUpDnCtl    = CreateUpDnCtl(hDlg);    // Create an Up-Down control.
            hwndProgBar    = CreateProgBar(hDlg);    // Create a Progress bar,
                                                     // to reflect the state of the Up-down control.

            return (INT_PTR)TRUE;

        case WM_NOTIFY:
            nCode = ((LPNMHDR)lParam)->code;

            switch (nCode)
            {
                case UDN_DELTAPOS:
                    lpnmud  = (LPNMUPDOWN)lParam;
                    iPosIndicated = SendMessage(hwndProgBar, PBM_GETPOS, (WPARAM)0, (LPARAM)0);

                    SendMessage(hwndProgBar,
                                PBM_SETPOS,
                                (WPARAM)(iPosIndicated + lpnmud->iDelta),  // iPosIndicated can have
                                (LPARAM)0);                                // any signed integer value.

                    break;
            }

        case WM_COMMAND:
            if (LOWORD(wParam) == IDOK || LOWORD(wParam) == IDCANCEL)
            {
                EndDialog(hDlg, LOWORD(wParam));
                return TRUE;
            }
            break;
    }
    return FALSE;
}

HWND CreateUpDnBuddy(HWND hwndParent)
{
    icex.dwICC = ICC_STANDARD_CLASSES;    // Set the Initialization Flag value.
    InitCommonControlsEx(&icex);          // Initialize the Common Controls Library to use 
                                          // Buttons, Edit Controls, Static Controls, Listboxes, 
                                          // Comboboxes, and  Scroll Bars.

    hControl = CreateWindowEx(WS_EX_LEFT | WS_EX_CLIENTEDGE | WS_EX_CONTEXTHELP,    //Extended window styles.
                              WC_EDIT,
                              NULL,
                              WS_CHILDWINDOW | WS_VISIBLE | WS_BORDER    // Window styles.
                              | ES_NUMBER | ES_LEFT,                     // Edit control styles.
                              rcClient.left+160, rcClient.top+40,
                              rcClient.left+52, rcClient.top+23,
                              hwndParent,
                              NULL,
                              g_hInst,
                              NULL);

    return (hControl);
}

HWND CreateUpDnCtl(HWND hwndParent)
{
    icex.dwICC = ICC_UPDOWN_CLASS;    // Set the Initialization Flag value.
    InitCommonControlsEx(&icex);      // Initialize the Common Controls Library.

    hControl = CreateWindowEx(WS_EX_LEFT | WS_EX_LTRREADING,
                              UPDOWN_CLASS,
                              NULL,
                              WS_CHILDWINDOW | WS_VISIBLE
                              | UDS_AUTOBUDDY | UDS_SETBUDDYINT | UDS_ALIGNRIGHT | UDS_ARROWKEYS | UDS_HOTTRACK,
                              0, 0,
                              0, 0,         // Set to zero to automatically size to fit the buddy window.
                              hwndParent,
                              NULL,
                              g_hInst,
                              NULL);

    SendMessage(hControl, UDM_SETRANGE, 0, MAKELPARAM(valMax, valMin));    // Sets the controls direction 
                                                                           // and range.

    return (hControl);
}
HWND CreateLabel(HWND hwndParent)
{
    hControl = CreateWindowEx(WS_EX_LEFT | WS_EX_LTRREADING,
                              WC_STATIC,
                              L"Adjust:",
                              WS_CHILDWINDOW | WS_VISIBLE | SS_RIGHT,
                              rcClient.left+100, rcClient.top+42,
                              rcClient.left+45, rcClient.top+23,
                              hwndParent,
                              NULL,
                              g_hInst,
                              NULL);

    return (hControl);
}
HWND CreateGroupBox(HWND hwndParent)
{
    hControl = CreateWindowEx(WS_EX_LEFT | WS_EX_CONTROLPARENT | WS_EX_LTRREADING,
                              WC_BUTTON,
                              L"Volume",
                              WS_CHILDWINDOW | WS_CLIPCHILDREN | WS_VISIBLE | WS_GROUP | BS_GROUPBOX,
                              rcClient.left+10, rcClient.top+10,
                              rcClient.right-20, rcClient.bottom-2*cyVScroll-10,
                              hwndParent,
                              NULL,
                              g_hInst,
                              NULL);

    return (hControl);
}
HWND CreateProgBar(HWND hwndParent)
{
    icex.dwICC = ICC_PROGRESS_CLASS;    // Set the Initialization Flag value.
    InitCommonControlsEx(&icex);        // Initialize the Common Controls Library to use the Progress Bar control.

    hControl = CreateWindowEx(WS_EX_STATICEDGE,
                              PROGRESS_CLASS,
                              L"Current Volume",
                              WS_CHILDWINDOW | WS_VISIBLE | PBS_SMOOTH,
                              rcClient.left+10, rcClient.bottom - cyVScroll-10,
                              rcClient.right-20, cyVScroll,
                              hwndParent,
                              NULL,
                              g_hInst,
                              NULL);

    // Set the range and increment of the progress bar.
    SendMessage(hControl, PBM_SETRANGE, 0, MAKELPARAM(0, 100));
    SendMessage(hControl, PBM_SETSTEP, (WPARAM) 1, 0);

    return (hControl);
}
```



## <a name="related-topics"></a><span data-ttu-id="cbaf4-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbaf4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbaf4-142">使用 Up-Down 控制項</span><span class="sxs-lookup"><span data-stu-id="cbaf4-142">Using Up-Down Controls</span></span>](using-up-down-controls.md)
</dt> <dt>

<span data-ttu-id="cbaf4-143">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="cbaf4-143">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 