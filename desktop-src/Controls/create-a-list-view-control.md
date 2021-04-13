---
title: 如何建立 List-View 控制項
description: 本主題將示範如何建立清單視圖控制項。 若要建立清單視圖控制項，請使用 CreateWindow 或 CreateWindowEx 函式，並指定 WC \_ LISTVIEW 視窗類別。
ms.assetid: FEAA0ACA-A086-46DF-9DD2-A3E32F2CCDA3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050498b87aaf701249a06cfe2c3ad18afdc1d84
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463944"
---
# <a name="how-to-create-a-list-view-control"></a><span data-ttu-id="4307a-104">如何建立 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="4307a-104">How to Create a List-View Control</span></span>

<span data-ttu-id="4307a-105">本主題將示範如何建立清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="4307a-105">This topic demonstrates how to create a list-view control.</span></span> <span data-ttu-id="4307a-106">若要建立清單視圖控制項，請使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定 [**WC \_ LISTVIEW**](common-control-window-classes.md) 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="4307a-106">To create a list-view control, you use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

<span data-ttu-id="4307a-107">您也可以建立清單視圖控制項作為對話方塊範本的一部分。</span><span class="sxs-lookup"><span data-stu-id="4307a-107">A list-view control can also be created as part of a dialog box template.</span></span> <span data-ttu-id="4307a-108">您必須指定 [**WC \_ LISTVIEW**](common-control-window-classes.md) 做為類別名稱。</span><span class="sxs-lookup"><span data-stu-id="4307a-108">You must specify [**WC\_LISTVIEW**](common-control-window-classes.md) as the class name.</span></span> <span data-ttu-id="4307a-109">若要使用清單視圖控制項作為對話方塊範本的一部分，您必須在建立對話方塊的實例之前，先呼叫 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 或 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 。</span><span class="sxs-lookup"><span data-stu-id="4307a-109">To use a list-view control as part of a dialog box template, you must call [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) or [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) before you create an instance of the dialog box.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="4307a-110">您必須知道的事項</span><span class="sxs-lookup"><span data-stu-id="4307a-110">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="4307a-111">技術</span><span class="sxs-lookup"><span data-stu-id="4307a-111">Technologies</span></span>

-   [<span data-ttu-id="4307a-112">Windows 控制項</span><span class="sxs-lookup"><span data-stu-id="4307a-112">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="4307a-113">必要條件</span><span class="sxs-lookup"><span data-stu-id="4307a-113">Prerequisites</span></span>

-   <span data-ttu-id="4307a-114">C/C++</span><span class="sxs-lookup"><span data-stu-id="4307a-114">C/C++</span></span>
-   <span data-ttu-id="4307a-115">Windows 消費者介面程式設計</span><span class="sxs-lookup"><span data-stu-id="4307a-115">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="4307a-116">指示</span><span class="sxs-lookup"><span data-stu-id="4307a-116">Instructions</span></span>


<span data-ttu-id="4307a-117">請先呼叫 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)函式，並在隨附的 **InitCommonControlsEx** 結構中指定 [**ICC \_ LISTVIEW \_ 類別**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)位，以註冊視窗類別。</span><span class="sxs-lookup"><span data-stu-id="4307a-117">First register the window class by calling the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function and specifying the [**ICC\_LISTVIEW\_CLASSES**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) bit in the accompanying **INITCOMMONCONTROLSEX** structure.</span></span> <span data-ttu-id="4307a-118">這可確保已載入通用控制項 DLL。</span><span class="sxs-lookup"><span data-stu-id="4307a-118">This ensures that the common controls DLL is loaded.</span></span> <span data-ttu-id="4307a-119">接下來，使用 [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) 或 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) 函式，並指定 [**WC \_ LISTVIEW**](common-control-window-classes.md) 視窗類別。</span><span class="sxs-lookup"><span data-stu-id="4307a-119">Next, use the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specify the [**WC\_LISTVIEW**](common-control-window-classes.md) window class.</span></span>

> [!Note]  
> <span data-ttu-id="4307a-120">依預設，清單視圖控制項會使用圖示標題字型。</span><span class="sxs-lookup"><span data-stu-id="4307a-120">By default, a list-view control uses the icon title font.</span></span> <span data-ttu-id="4307a-121">不過，您可以使用 [**WM \_ SETFONT**](/windows/desktop/winmsg/wm-setfont) 訊息來指定要用於文字的字型。</span><span class="sxs-lookup"><span data-stu-id="4307a-121">However, you can use a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to specify the font to be used for the text.</span></span> <span data-ttu-id="4307a-122">您應該先傳送此訊息，然後再插入任何專案。</span><span class="sxs-lookup"><span data-stu-id="4307a-122">You should send this message before inserting any items.</span></span> <span data-ttu-id="4307a-123">控制項會使用由 **WM \_ SETFONT** 訊息所指定的字型維度來判斷間距和版面配置。</span><span class="sxs-lookup"><span data-stu-id="4307a-123">The control uses the dimensions of the font that is specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span> <span data-ttu-id="4307a-124">您也可以自訂每個專案的字型。</span><span class="sxs-lookup"><span data-stu-id="4307a-124">You can also customize the font for each item.</span></span> <span data-ttu-id="4307a-125">如需詳細資訊，請參閱 [自訂繪製](custom-draw.md)。</span><span class="sxs-lookup"><span data-stu-id="4307a-125">For more information, see [Custom Draw](custom-draw.md).</span></span>

 

<span data-ttu-id="4307a-126">下列 c + + 程式碼範例會在報表檢視中建立清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="4307a-126">The following C++ code example creates a list-view control in report view.</span></span>


```C++
// CreateListView: Creates a list-view control in report view.
// Returns the handle to the new control
// TO DO:  The calling procedure should determine whether the handle is NULL, in case 
// of an error in creation.
//
// HINST hInst: The global handle to the applicadtion instance.
// HWND  hWndParent: The handle to the control's parent window. 
//
HWND CreateListView (HWND hwndParent) 
{
    INITCOMMONCONTROLSEX icex;           // Structure for control initialization.
    icex.dwICC = ICC_LISTVIEW_CLASSES;
    InitCommonControlsEx(&icex);

    RECT rcClient;                       // The parent window's client area.

    GetClientRect (hwndParent, &rcClient); 

    // Create the list-view window in report view with label editing enabled.
    HWND hWndListView = CreateWindow(WC_LISTVIEW, 
                                     L"",
                                     WS_CHILD | LVS_REPORT | LVS_EDITLABELS,
                                     0, 0,
                                     rcClient.right - rcClient.left,
                                     rcClient.bottom - rcClient.top,
                                     hwndParent,
                                     (HMENU)IDM_CODE_SAMPLES,
                                     g_hInst,
                                     NULL); 

    return (hWndListView);
}

```




<span data-ttu-id="4307a-127">一般而言，清單視圖應用程式可讓使用者從某個視圖變更為另一個視圖。</span><span class="sxs-lookup"><span data-stu-id="4307a-127">Typically, list-view applications enable the user to change from one view to another.</span></span>

<span data-ttu-id="4307a-128">下列 c + + 程式碼範例會變更清單視圖的視窗樣式，進而變更視圖。</span><span class="sxs-lookup"><span data-stu-id="4307a-128">The following C++ code example changes the list-view's window style, which in turn changes the view.</span></span>


```C++
// SetView: Sets a list-view's window style to change the view.
// hWndListView: A handle to the list-view control. 
// dwView:       A value specifying the new view style.
//
VOID SetView(HWND hWndListView, DWORD dwView) 
{ 
    // Retrieve the current window style. 
    DWORD dwStyle = GetWindowLong(hWndListView, GWL_STYLE); 
    
    // Set the window style only if the view bits changed.
    if ((dwStyle & LVS_TYPEMASK) != dwView) 
    {
        SetWindowLong(hWndListView,
                      GWL_STYLE,
                      (dwStyle & ~LVS_TYPEMASK) | dwView);
    }               // Logical OR'ing of dwView with the result of 
}                   // a bitwise AND between dwStyle and 
                    // the Unary complenent of LVS_TYPEMASK.

```



## <a name="related-topics"></a><span data-ttu-id="4307a-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="4307a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4307a-130">清單視圖控制項參考</span><span class="sxs-lookup"><span data-stu-id="4307a-130">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="4307a-131">關於 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="4307a-131">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="4307a-132">使用 List-View 控制項</span><span class="sxs-lookup"><span data-stu-id="4307a-132">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 