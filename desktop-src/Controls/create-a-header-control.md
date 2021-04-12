---
title: 如何建立標題控制項
description: 本主題將示範如何建立標題控制項，並將它放在父視窗的工作區中。
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104024355"
---
# <a name="how-to-create-a-header-control"></a><span data-ttu-id="f28ae-103">如何建立標題控制項</span><span class="sxs-lookup"><span data-stu-id="f28ae-103">How to Create a Header Control</span></span>

<span data-ttu-id="f28ae-104">本主題將示範如何建立標題控制項，並將它放在父視窗的工作區中。</span><span class="sxs-lookup"><span data-stu-id="f28ae-104">This topic demonstrates how to create a header control and position it within the parent window's client area.</span></span> <span data-ttu-id="f28ae-105">您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立標題控制項，並指定 [**WC \_ 標頭**](common-control-window-classes.md) 視窗類別和適當的 [標題控制項樣式](header-control-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="f28ae-105">You can create a header control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**WC\_HEADER**](common-control-window-classes.md) window class and the appropriate [header control styles](header-control-styles.md).</span></span> <span data-ttu-id="f28ae-106">載入通用控制項 DLL 時，會註冊此視窗類別。</span><span class="sxs-lookup"><span data-stu-id="f28ae-106">This window class is registered when the common control DLL is loaded.</span></span> <span data-ttu-id="f28ae-107">若要確定已載入此 DLL，請使用 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函數。</span><span class="sxs-lookup"><span data-stu-id="f28ae-107">To ensure that this DLL is loaded, use the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f28ae-108">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="f28ae-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f28ae-109">技術</span><span class="sxs-lookup"><span data-stu-id="f28ae-109">Technologies</span></span>

-   [<span data-ttu-id="f28ae-110">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="f28ae-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f28ae-111">必要條件</span><span class="sxs-lookup"><span data-stu-id="f28ae-111">Prerequisites</span></span>

-   <span data-ttu-id="f28ae-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="f28ae-112">C/C++</span></span>
-   <span data-ttu-id="f28ae-113">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="f28ae-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f28ae-114">指示</span><span class="sxs-lookup"><span data-stu-id="f28ae-114">Instructions</span></span>


<span data-ttu-id="f28ae-115">下列 c + + 程式碼範例會先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式來載入通用控制項 DLL。</span><span class="sxs-lookup"><span data-stu-id="f28ae-115">The following C++ code example first calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="f28ae-116">然後，它會呼叫 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式來建立標題控制項。</span><span class="sxs-lookup"><span data-stu-id="f28ae-116">It then calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a header control.</span></span> <span data-ttu-id="f28ae-117">控制項一開始是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="f28ae-117">The control is initially hidden.</span></span> <span data-ttu-id="f28ae-118">[**HDM \_ 版面**](hdm-layout.md)配置訊息是用來計算控制項在父視窗內的大小與位置。</span><span class="sxs-lookup"><span data-stu-id="f28ae-118">The [**HDM\_LAYOUT**](hdm-layout.md) message is used to calculate the size and position of the control within the parent window.</span></span> <span data-ttu-id="f28ae-119">然後，控制項會重新置放並使其成為可見。</span><span class="sxs-lookup"><span data-stu-id="f28ae-119">The control is then repositioned and made visible.</span></span>



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a><span data-ttu-id="f28ae-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="f28ae-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f28ae-121">關於標題控制項</span><span class="sxs-lookup"><span data-stu-id="f28ae-121">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="f28ae-122">標題控制項參考</span><span class="sxs-lookup"><span data-stu-id="f28ae-122">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="f28ae-123">使用標題控制項</span><span class="sxs-lookup"><span data-stu-id="f28ae-123">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 