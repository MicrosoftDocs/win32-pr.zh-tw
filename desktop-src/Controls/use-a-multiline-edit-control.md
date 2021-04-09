---
title: 如何建立多行編輯控制項
description: 本主題將示範如何藉由將多行編輯控制項新增至視窗的工作區，來執行簡單的單字處理器。
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933730"
---
# <a name="how-to-create-a-multiline-edit-control"></a><span data-ttu-id="73973-103">如何建立多行編輯控制項</span><span class="sxs-lookup"><span data-stu-id="73973-103">How to Create a Multiline Edit Control</span></span>

<span data-ttu-id="73973-104">本主題將示範如何藉由將多行編輯控制項新增至視窗的工作區，來執行簡單的單字處理器。</span><span class="sxs-lookup"><span data-stu-id="73973-104">This topic demonstrates how to implement a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="73973-105">藉由使用多行編輯控制項，使用者可以從功能表選取 [編輯命令]。</span><span class="sxs-lookup"><span data-stu-id="73973-105">By using the multiline edit control, the user can select edit commands from a menu.</span></span> <span data-ttu-id="73973-106">這些命令可讓使用者執行簡單的編輯作業，例如復原先前的動作、剪下或複製剪貼簿的選取專案、貼上剪貼簿中的文字，以及刪除目前的選取專案。</span><span class="sxs-lookup"><span data-stu-id="73973-106">These commands enable the user to perform simple editing operations such as undo a previous action, cut or copy selections to the clipboard, paste text from the clipboard, and delete the current selection.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="73973-107">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="73973-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="73973-108">技術</span><span class="sxs-lookup"><span data-stu-id="73973-108">Technologies</span></span>

-   [<span data-ttu-id="73973-109">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="73973-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="73973-110">必要條件</span><span class="sxs-lookup"><span data-stu-id="73973-110">Prerequisites</span></span>

-   <span data-ttu-id="73973-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="73973-111">C/C++</span></span>
-   <span data-ttu-id="73973-112">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="73973-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="73973-113">指示</span><span class="sxs-lookup"><span data-stu-id="73973-113">Instructions</span></span>


<span data-ttu-id="73973-114">您的應用程式必須包含程式碼，以建立的實例，並初始化多行編輯控制項，然後處理使用者編輯命令。</span><span class="sxs-lookup"><span data-stu-id="73973-114">Your application must include code to create an instance of and initialize a multiline edit control and then process user edit commands.</span></span>

<span data-ttu-id="73973-115">下列 c + + 程式碼範例會藉由將多行編輯控制項新增至視窗的工作區，來實作為簡單字處理器的大部分功能。</span><span class="sxs-lookup"><span data-stu-id="73973-115">The following C++ code example implements much of the functionality of a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="73973-116">系統會自動執行編輯控制項的 wordwrap 作業，也會處理垂直捲動條的處理， (藉由在) 的 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa)函式呼叫中指定 [**ES \_ AUTOVSCROLL**](edit-control-styles.md)來建立。</span><span class="sxs-lookup"><span data-stu-id="73973-116">The system automatically performs wordwrap operations for the edit control and also handles the processing for the vertical scroll bar (created by specifying [**ES\_AUTOVSCROLL**](edit-control-styles.md) in the call to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function).</span></span>

<span data-ttu-id="73973-117">使用者編輯命令會透過 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 通知訊息傳送至視窗進程。</span><span class="sxs-lookup"><span data-stu-id="73973-117">User edit commands are sent to the window process via [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages.</span></span>

> [!Note]  
> <span data-ttu-id="73973-118">如果視窗包含 Windows 功能區，則必須調整編輯控制項的大小，以容納功能區的高度。</span><span class="sxs-lookup"><span data-stu-id="73973-118">If the window includes the Windows Ribbon, the size of the edit control must be adjusted to accommodate the height of the Ribbon.</span></span> <span data-ttu-id="73973-119">如需詳細資訊，請參閱 [Windows 功能區架構](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry)。</span><span class="sxs-lookup"><span data-stu-id="73973-119">For more information, see [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span></span>

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="related-topics"></a><span data-ttu-id="73973-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="73973-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73973-121">關於編輯控制項</span><span class="sxs-lookup"><span data-stu-id="73973-121">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="73973-122">編輯控制項參考</span><span class="sxs-lookup"><span data-stu-id="73973-122">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="73973-123">使用編輯控制項</span><span class="sxs-lookup"><span data-stu-id="73973-123">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="73973-124">編輯控制項</span><span class="sxs-lookup"><span data-stu-id="73973-124">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 