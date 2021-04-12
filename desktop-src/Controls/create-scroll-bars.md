---
title: 如何建立捲軸
description: 建立重迭、快顯視窗或子視窗時，您可以使用 CreateWindowEx 函式，並指定 WS \_ HSCROLL、WS \_ VSCROLL 或這兩種樣式來新增標準捲軸。
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b27e3e6d9495492f46567633cc53b0f3f7c5bd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463801"
---
# <a name="how-to-create-scroll-bars"></a><span data-ttu-id="93794-103">如何建立捲軸</span><span class="sxs-lookup"><span data-stu-id="93794-103">How to Create Scroll Bars</span></span>

<span data-ttu-id="93794-104">建立重迭、快顯視窗或子視窗時，您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定 ws \_ HSCROLL、WS \_ VSCROLL 或這兩種樣式來新增標準捲軸。</span><span class="sxs-lookup"><span data-stu-id="93794-104">When creating an overlapped, pop-up, or child window, you can add standard scroll bars by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying WS\_HSCROLL, WS\_VSCROLL, or both styles.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="93794-105">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="93794-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="93794-106">技術</span><span class="sxs-lookup"><span data-stu-id="93794-106">Technologies</span></span>

-   [<span data-ttu-id="93794-107">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="93794-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="93794-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="93794-108">Prerequisites</span></span>

-   <span data-ttu-id="93794-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="93794-109">C/C++</span></span>
-   <span data-ttu-id="93794-110">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="93794-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="93794-111">指示</span><span class="sxs-lookup"><span data-stu-id="93794-111">Instructions</span></span>

### <a name="create-a-scroll-bar"></a><span data-ttu-id="93794-112">建立捲軸</span><span class="sxs-lookup"><span data-stu-id="93794-112">Create a Scroll Bar</span></span>

<span data-ttu-id="93794-113">下列範例會建立具有標準水準和垂直捲動條的視窗。</span><span class="sxs-lookup"><span data-stu-id="93794-113">The following example creates a window with standard horizontal and vertical scroll bars.</span></span>


```C++
    hwnd = CreateWindowEx( 
        0,                     // no extended styles 
        g_szWindowClass,       // global string containing name of window class
        g_szTitle,             // global string containing title bar text 
        WS_OVERLAPPEDWINDOW |  
            WS_HSCROLL | WS_VSCROLL, // window styles 
        CW_USEDEFAULT,         // default horizontal position 
        CW_USEDEFAULT,         // default vertical position 
        CW_USEDEFAULT,         // default width 
        CW_USEDEFAULT,         // default height 
        (HWND) NULL,           // no parent for overlapped windows 
        (HMENU) NULL,          // use the window class menu 
        g_hInst,               // global instance handle  
        (PVOID) NULL           // pointer not needed 
    ); 
```



<span data-ttu-id="93794-114">若要處理這些捲軸的捲軸訊息，您必須在主視窗程式中包含適當的程式碼。</span><span class="sxs-lookup"><span data-stu-id="93794-114">To process scroll bar messages for these scroll bars, you must include appropriate code in the main window procedure.</span></span>

<span data-ttu-id="93794-115">您可以使用 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，藉由指定捲軸視窗類別來建立捲軸。</span><span class="sxs-lookup"><span data-stu-id="93794-115">You can use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a scroll bar by specifying the SCROLLBAR window class.</span></span> <span data-ttu-id="93794-116">這會根據 [**sbs \_ HORZ**](scroll-bar-control-styles.md) 或 [**sbs \_ 垂直**](scroll-bar-control-styles.md) 是否指定為視窗樣式，建立水準或垂直捲動條。</span><span class="sxs-lookup"><span data-stu-id="93794-116">This creates a horizontal or vertical scroll bar, depending on whether [**SBS\_HORZ**](scroll-bar-control-styles.md) or [**SBS\_VERT**](scroll-bar-control-styles.md) is specified as the window style.</span></span> <span data-ttu-id="93794-117">也可以指定捲軸大小及其父視窗的相對位置。</span><span class="sxs-lookup"><span data-stu-id="93794-117">The scroll bar size and its position relative to its parent window can also be specified.</span></span>

<span data-ttu-id="93794-118">下列範例會建立在父視窗的工作區底部放置的水準捲軸。</span><span class="sxs-lookup"><span data-stu-id="93794-118">The following example creates a horizontal scroll bar that is positioned along the bottom of the parent window's client area.</span></span>


```C++
// Description:
//   Creates a horizontal scroll bar along the bottom of the parent 
//   window's area.
// Parameters:
//   hwndParent - handle to the parent window.
//   sbHeight - height, in pixels, of the scroll bar.
// Returns:
//   The handle to the scroll bar.
HWND CreateAHorizontalScrollBar(HWND hwndParent, int sbHeight)
{
    RECT rect;

    // Get the dimensions of the parent window's client area;
    if (!GetClientRect(hwndParent, &rect))
        return NULL;

    // Create the scroll bar.
    return (CreateWindowEx( 
            0,                      // no extended styles 
            L"SCROLLBAR",           // scroll bar control class 
            (PTSTR) NULL,           // no window text 
            WS_CHILD | WS_VISIBLE   // window styles  
                | SBS_HORZ,         // horizontal scroll bar style 
            rect.left,              // horizontal position 
            rect.bottom - sbHeight, // vertical position 
            rect.right,             // width of the scroll bar 
            sbHeight,               // height of the scroll bar
            hwndParent,             // handle to main window 
            (HMENU) NULL,           // no menu 
            g_hInst,                // instance owning this window 
            (PVOID) NULL            // pointer not needed 
        )); 
}
```



## <a name="related-topics"></a><span data-ttu-id="93794-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="93794-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93794-120">使用捲軸</span><span class="sxs-lookup"><span data-stu-id="93794-120">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="93794-121">[Windows 通用控制項示範 (CppWindowsCommonControls) ](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="93794-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 